# MaskContainer

[`MaskContainer`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/MaskContainer/index.js) is a component to wrap asynchronous blocks based on [STATUS](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/docs/components/src/constants/status.js).

It shows an icon loader indicator while requests are being loaded or an Error icon when they fail.

## Props

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| className | string | className applied to wrapper element. |  |
| display | oneOf\('absolute', 'fixed'\) | position applied to wrapper element. | fixed |
| minHeight | number,string | minHeight applied to wrapper element. | 400 |
| handleFailed | bool | determinates if MaskContainer will handle the FAILED status. | true |
| showIndicator | bool | loading & error icons indicator visibility. | true |
| status | oneOf\([Status constants](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/docs/components/src/constants/status.js)\) | component status. |  |

