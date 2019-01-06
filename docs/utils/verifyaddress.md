# verifyAddress

In the US, we validate addresses using [Smarty Streets](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/docs/utils/`https:/smartystreets.com`). This cuts down on invalid addresses making their way to fulfillment at the warehouse.

Use [`verifyAddress`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Addresses/verifyAddress.js) in a [`Form`](../components/form.md) `onBeforeSubmit` to verify an address with Smarty Streets before submitting.

