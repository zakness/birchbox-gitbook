# ButtonGroup

[`ButtonGroup`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/ButtonGroup/index.js) wraps multiple `Button`-like or `TextInput` components and does the following:

* Collapses their sides & borders by setting the `buttonGroup` prop
* Makes sure they are equal width via flex-basis \(you can override this with the `equalize` prop\)

```text
<ButtonGroup>
  <Button preset='primaryStroke' onClick={...}>Cancel</Button>
  <Button preset='primary' onClick={...}>Continue</Button>
</ButtonGroup>

<ButtonGroup equalize={false}>
  <TextInput label='Email Address' />
  <Button preset='primary' onClick={...}>Submit</Button>
</ButtonGroup>
```

**Width**

By default `ButtonGroup` will use the children’s content width for sizing. If you would prefer to fill the container, set the `fullWidth` prop to `true`.

_Note: In the Non-Evo wide breakpoint,_ `ButtonGroup`_’s width is based on the old_ `widthButtonPairStandard` _value \(since button styles from_ `button.css` _are all full-width\)._

**Stacking**

Sometimes, especially on some mobile devices, the children do not quite fit side-by-side. When this happens you should set the `stacked` prop to `true` to have the children stacked on top of each other. When stacked, the children’s abutting sides are _not_ collapsed like they are when side-by-side.

```text
// Now Continue is on top of Cancel in the narrow breakpoint
<ButtonGroup stacked={props.isBreakpointNarrow}>
  <Button preset='primaryStroke' onClick={...}>Cancel</Button>
  <Button preset='primary' onClick={...}>Continue</Button>
</ButtonGroup>
```

This uses `flex-direction: column-reverse` so the right-most button will appear on top.

