# SimplebillyApi::TrackOrderResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |
| **order_status** | **String** |  |  |
| **shipments** | [**Array&lt;TrackedShipment&gt;**](TrackedShipment.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TrackOrderResponse.new(
  order_number: null,
  order_status: null,
  shipments: null
)
```

