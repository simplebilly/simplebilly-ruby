# SimplebillyApi::TrackedShipment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **carrier** | **String** |  |  |
| **events** | [**Array&lt;TrackingEvent&gt;**](TrackingEvent.md) |  |  |
| **label_url** | **String** |  | [optional] |
| **status** | **String** |  |  |
| **tracking_number** | **String** |  | [optional] |
| **tracking_url** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TrackedShipment.new(
  carrier: null,
  events: null,
  label_url: null,
  status: null,
  tracking_number: null,
  tracking_url: null
)
```

