# CreditCardFields

[`CreditCardFields`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Payment/CreditCardFields/index.js) is a group of four fields that capture a credit card. Uses [`Form2Beta`](form.md) paradigms.

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| fieldProps | arrayOf\(fieldProps\) | Field props. Typically passed down from parent `Form`. |  |
| namePrefix | string | Dot-notated prefix for the credit card field names. Used if the credit card fields are nested in the form data. |  |
| onChange | \(data\) =&gt; ? | Handles changes to field data. Typically passed down from parent `Form`. |  |
| onCreditCardNumberFocus | \(\) =&gt; ? | Called when the user focuses the credit card number field. |  |

## Credit card shape

```text
{
  creditCardNumber: '4100500000000000',
  expirationMonth: '02',
  expirationYear: '19',
  cvv: '031',
}
```

## Example implementation

* [CheckoutView/AddNewCreditCard](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/views/checkout/CheckoutView/AddNewCreditCard/index.js) — Choosing to use a new credit card in checkout.

