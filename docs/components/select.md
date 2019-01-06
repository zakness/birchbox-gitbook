# Select

[`Select`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Form2Beta/Select/index.js) is a [controlled](https://facebook.github.io/react/docs/forms.html#controlled-components) `<select>` component.

Designed to be used with [`Form2Beta`](form.md).

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| isInvalid | bool | Render with invalid styling? | `false` |
| isOptional | bool | Can have an empty value upon submission? If `true`, “ \(optional\)” is appended to the label display. | `false` |
| label | string | User-facing field label. |  |
| name | string | Identifying data key. |  |
| onChange | \({ \[name\]: value }\) =&gt; ? | Passes up changes to field data. |  |
| options | arrayOf\({ label, value }\) | List of options. Both labels and values can be strings or numbers. | `[]` |
| value | string\|number | Selected value. | `options[0]` |

Where possible, props are typically passed down from a parent `Form`.

