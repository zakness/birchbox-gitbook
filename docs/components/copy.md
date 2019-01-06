# Copy

[`Copy`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Copy/index.js) is a [Markdown](markdown.md) component that can have a particular font color and size applied. One use case for Copy is for CMS components that provide Markdown fields with customizable font size and color.

## props

### className

```text
PropTypes.string
```

Passed through to the Markdown component.

### color

```text
PropTypes.string
```

The text color. Can be a color name \(`colorTurquoise`\), theme color name \(`majorColorDark`\), or hex code \(`#41b1c0`\).

### content

```text
PropTypes.string
```

Markdown content passed through to the Markdown component.

### copySize

```text
PropTypes.string
```

Sets the type style \(font family and size\). Must be one of the styled-component utilities exported from [styleds/copySizes](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/styleds/copySizes.js).

