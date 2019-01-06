# LinkClickable

Use [`LinkClickable`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/LinkClickable/index.js) if you want a `Clickable` that looks like a `Link`.

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| children | `node` | LinkClickable children |  |
| className | string | Passed through. |  |
| colorPair | array | Two colorNames for link's underline states, default and hover respectively | \[ 'majorColorDark', 'majorColorLight' \] |
| disabled | bool | If true, prevents `onClick` from executing and applies `disabled` styling | false |
| decorate | bool | If true, adds the default `<a>` styling. | false |
| onClick | func | Thing to do on click |  |
| onHoverChange | func\(hovering:bool\) | Triggered with `true` when mouse enters element, `false` when mouse leaves |  |
| trackingProps | obj | Object containing any event tracking data to be logged onClick. More on the logging properties [here](../utils/logging.md) |  |

