# RefWrapper

If you need to set a `ref` on a stateless functional component, you must wrap that component with [`RefWrapper`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/RefWrapper/index.js) otherwise the value passed to the `ref` function will be `null`. See [issue discussion](https://github.com/facebook/react/issues/4936).

## Example

A higher order component wants access to all of its children \(recursive\) with a `special` prop:

```text
class HigherOrderComponent extends React.Component {
  constructor (props) {
    super(props)
    this.specialRefs = {}
  }

  render () {
    return <div>
      {this.getChildrenWithRefs(this.props.children)}
      <div>
        {_.map(_.keys(this.specialRefs), (key) => (
          <div key={`special-${key}`} onClick={this.doSomething.bind(this, key)}>{key}</div>
        ))}
      </div>
    </div>
  }

  getChildrenWithRefs (children) {
    if (!children) {
      return children
    }
    const childrenWithRefs = React.Children.map(children, (child) => {
      const special = child.props.special
      const clone = React.cloneElement(child, {}, this.getChildrenWithRefs(child.props.children))
      if (special) {
        return <RefWrapper ref={(node) => this.specialRefs[special] = node}>{clone}</RefWrapper>
      }
      return clone
    })
    return childrenWithRefs
  }

  doSomething (key) {
    const node = ReactDOM.findDOMNode(this.scrollRefs[key])
    // do something
  }
}
```

