# AddressForm

[`AddressForm`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Addresses/AddressForm/index.js) is a form that capture an address. Essentially wraps [AddressFields](addressfields.md) in a [Form](form.md) with submit and cancel buttons.

Not sure this is the right component for your use case? See [other address-related components](../guides/addresses.md).

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| allowCancel | bool | Show the cancel button? | `true` |
| cancel | \(\) =&gt; ? | Function executed when the cancel button is clicked. |  |
| submit | \({ address }\) =&gt; Promise | Function that does something with the address data upon form submission. |  |

