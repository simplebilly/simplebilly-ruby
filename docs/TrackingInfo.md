# SimplebillyApi::TrackingInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **carrier** | **String** |  |  |
| **estimated_delivery** | **String** |  | [optional] |
| **events** | [**Array&lt;TrackingEvent&gt;**](TrackingEvent.md) |  |  |
| **raw_response** | **Object** |  | [optional] |
| **status** | **String** |  |  |
| **tracking_number** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TrackingInfo.new(
  carrier: null,
  estimated_delivery: null,
  events: null,
  raw_response: null,
  status: null,
  tracking_number: null
)
```

