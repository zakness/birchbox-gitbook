# PaymentUsageCheckboxes

[`PaymentUsageCheckboxes`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Payment/PaymentUsageCheckboxes/index.js) is a group of checkboxes that represent how a payment profile is used by the system. For example for subscription billing. Uses [`Form2Beta`](form.md) paradigms. This component is typically used with [CreditCardFields](creditcardfields.md).

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| initialData | object | Payment usage object \(see shape below\) representing how the payment profile is currently used. These values cannot be unchecked. |  |
| fieldProps | arrayOf\(fieldProps\) | Field props. Typically passed down from parent `Form`. |  |
| onChange | \(data\) =&gt; ? | Handles changes to field data. Typically passed down from parent `Form`. |  |

## Payment usage shape

```text
{
  isWomensSubscriptionBilling: false,
  isMensSubscriptionBilling: false,
}
```

## Example implementation

* [MyAccountView/PaymentForm](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/views/account/MyAccountView/PaymentDetails/PaymentForm/index.js) — A form for editing or creating a payment profile.

