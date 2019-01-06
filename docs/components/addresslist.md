# AddressList

[`AddressList`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Addresses/AddressList/index.js) displays a list of addresses, allowing the user to pick one.

Not sure this is the right component for your use case? See [other address-related components](../guides/addresses.md).

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| addresses | arrayOf\(address\) | List of addresses. | `[]` |
| selectedAddressId | number | Id of selected address. |  |
| onSelect | \(id\) =&gt; ? | Function executed when a user clicks an unselected address. |  |

