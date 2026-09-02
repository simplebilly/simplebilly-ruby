# SimplebillyApi::ShipmentStatusUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivered_at** | **String** |  | [optional] |
| **signed_by** | **String** |  | [optional] |
| **status** | **String** |  |  |
| **tracking_number** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ShipmentStatusUpdate.new(
  delivered_at: null,
  signed_by: null,
  status: null,
  tracking_number: null
)
```

