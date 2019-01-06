# logging

## Logging Events

Event data should be logged via the utility function `log`. This function takes a JSON object which contains all relevant data to be passed to external tracking.

```text
import { log } from 'utils/logging'

log({
  event: 'click',
  mod: 'site-content',
  title: e.target.innerText || '[non-text content]',
  type: 'button',
})
```

NB: All `Link` and `Clickable` interactions are already logged, as well as all page views. You should only need to use `log` to add custom events, e.g.

```text
log({
  context: 'session',
  event: 'register-experiment',
  feature: 'xm',
  variant: data[version].name,
  iteration,
  version,
})
```

## Logging Event Properties

### event

The `event` property is required. This property should describe the type of event being logged, e.g. 'click', 'view', etc.

### context

The `context` property can be passed in as part of the event data payload. If it is not set it will be set to the current `pageType` value, defined in the view route.

### path

The `path` property \(equivalent to `window.location.pathname`\) is automatically added to all event.api events.

### vertical

The `vertical` property is automatically added to all logging events.

## Console debugging

Console log messages can be enabled via localStorage flags.

Log tracking event data:

```text
localStorage.setItem('debugTracking', true)
```

Log event.api payload data:

```text
localStorage.setItem('debugEventApi', true)
```

Log tag manager data:

```text
localStorage.setItem('debugTagManager', true)
```

## Registering an Experiment Variant

When running experiments, we must make a logging call that registers a given session for the specific experiment variant assigned to the user. Use the `logExperiment` utility method to make this call:

```text
import { logExperiment } from 'utils/logging'

logExperiment('experiment-name', 'variant-name')
```

This call is memoized on its arguments so the same registration call is not made more than once per session \(it would be okay to do so, it’s just unnecessary\).

