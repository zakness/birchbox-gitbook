# DropdownMenu

[`DropdownMenu`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/DropdownMenu/index.js) is a standalone menu that looks like a custom `<select>`. It is “standalone” because its styling does not match other form components and it is not meant to be used in that context. It is meant to be used as an action trigger such as review filtering.

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| onSelect | func\(value\) | Called when a menu item is clicked, passing the item’s value |  |
| options | arrayOf\({ label, value }\) | List of label+value pairs. |  |
| value | any | The selected value |  |
| width | string\|number | CSS width value | 'auto' |

