# AddressFields

[`AddressFields`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Addresses/AddressFields/index.js) is a group of fields that capture an address. Uses [`Form2Beta`](form.md) paradigms. Use this component if you want to capture an address _along with other data_ in a form.

Not sure this is the right component for your use case? See [other address-related components](../guides/addresses.md).

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| fieldProps | arrayOf\(fieldProps\) | Field props. Typically passed down from parent `Form`. |  |
| namePrefix | string | Dot-notated prefix for the address field names. Used if the address fields are nested in the form data. |  |
| onChange | \(data\) =&gt; ? | Handles changes to field data. Typically passed down from parent `Form`. |  |
| countryWhitelist | arrayOf\(countryCodes\) | Country codes array to determine which countries are allowed to use in form. if not set all locale countries get set by default. countryWhitelist shape example: \['US', 'GU', 'VI'\] |  |
| regionValueFormat | oneOf\('regionCode', 'name'\) | This property determine if select its going to use either regionCode or name as value | 'name' |

## Address shape

```text
{
  city: 'New York',
  company: 'Birchbox',
  country: 'US',
  firstName: 'Zach',
  lastName: 'Lindner',
  postCode: '10017',
  state: 'New York',
  streetAddress1: '115 Lexington Ave',
  streetAddress2: 'Apt 3',
  telephone: '999999999',
}
```

## Example implementation

* [components/AddressForm](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Addresses/AddressForm/index.js) — A generic address form for capturing basic address data.

