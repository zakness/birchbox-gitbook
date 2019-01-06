# PageViewDispatcher

[← Routing docs](../guides/routing/)

## `<PageViewDispatcher>`

When [`<PageViewDispatcher>`](https://github.com/zakness/birchbox-gitbook/tree/1ad9356b440d8ffd191f6222475ef6f0c15444b0/src/components/Routing/PageViewDispatcher/index.js) mounts or renders with a new [`location`](../guides/routing/routing-redux-state.md#location) it disptaches `PAGE_VIEW`, signifying that we have viewed a new page \(the last phase of a [navigation event](../guides/routing/routing-navigation-event.md)\).

`<PageViewDispatcher>` is typically the direct parent of a view component.

### Props

Most of `<PageViewDispatcher>`’s props are mapped from the [`router.next`](../guides/routing/routing-redux-state.md#routernext) state, but there is one prop that can be manually set — `logParams`. Use this prop if you want to add more data to the `page-view` log event that gets fired on `PAGE_VIEW`.

| Prop | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| logParams | object | Additional parameters to add to the `page-view` logging event |  |

