# Separator

[`Separator`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Separator/index.js) is a styled `<div>` that renders as a vertical or horizontal line.

**Note:** Separator is [adapted](../enhancers/adapter.md), so you can specify breakpoint value objects as any of its props.

## Example

```text
<Separator
  color={{ wide: 'colorNeutral9F' }}
  length={{ wide: unit16 }}
  margin={{ narrow: `${unit12} ${unit24}` }}
  orientation={{ narrow: 'horizontal', wide: 'vertical' }}
/>
```

## Props

### className

```text
PropTypes.string
```

Passed through. The rest of the props try to account for most use cases, so ideally this is only necessary for complex cases.

### color

```text
PropTypes.string
```

The color of the line. Can be a hex code, color variable name, or theme color name.

Defaults to `colorNeutralCD`.

### length

```text
PropTypes.oneOfType([ PropTypes.string, PropTypes.number ])
```

How long should the line be? If number, it’s converted to `px`.

There is no default, so horizontal lines will extend the length of their container.

### margin

```text
PropTypes.oneOfType([ PropTypes.string, PropTypes.number ])
```

Value for the CSS `margin` property. This could also be achieved using `className`, but adding margins is a very common use case.

### thickness

```text
PropTypes.oneOfType([ PropTypes.string, PropTypes.number ])
```

How thick should the line be? If number, it’s converted to `px`.

Defaults to `1`.

### orientation

```text
PropTypes.oneOf([ 'vertical', 'horizontal' ])
```

Is the line vertical or horizontal?

Defaults to `horizontal`.

