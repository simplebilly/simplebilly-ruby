# SimplebillyApi::WebhookEvent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attempts** | **Integer** |  | [optional] |
| **channel** | **String** | source for inbound, target URL for outbound. | [optional] |
| **direction** | [**WebhookDirection**](WebhookDirection.md) | inbound | outbound |  |
| **event_type** | **String** |  |  |
| **last_error** | **String** |  | [optional] |
| **payload** | **Object** |  | [optional] |
| **status** | [**WebhookEventStatus**](WebhookEventStatus.md) | accepted | delivered | failed | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::WebhookEvent.new(
  attempts: null,
  channel: null,
  direction: null,
  event_type: null,
  last_error: null,
  payload: null,
  status: null
)
```

