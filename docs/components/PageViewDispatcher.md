[← Routing docs](/docs/guides/Routing.md)

# `<PageViewDispatcher>`

When [`<PageViewDispatcher>`](/src/components/Routing/PageViewDispatcher/index.js) mounts or renders with a new [`location`](/docs/guides/Routing-redux-state.md#location) it disptaches `PAGE_VIEW`, signifying that we have viewed a new page (the last phase of a [navigation event](/docs/guides/Routing-navigation-event.md)).

`<PageViewDispatcher>` is typically the direct parent of a view component.

## Props

Most of `<PageViewDispatcher>`’s props are mapped from the [`router.next`](/docs/guides/Routing-redux-state.md#routernext) state, but there is one prop that can be manually set — `logParams`. Use this prop if you want to add more data to the `page-view` log event that gets fired on `PAGE_VIEW`.

Prop|Type|Description|Default
---|---|---|---
logParams|object|Additional parameters to add to the `page-view` logging event|
