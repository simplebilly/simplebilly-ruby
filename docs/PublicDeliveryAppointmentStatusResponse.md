# SimplebillyApi::PublicDeliveryAppointmentStatusResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **appointment_id** | **String** |  |  |
| **requested_date** | **Date** |  |  |
| **status** | **String** |  |  |
| **time_slot** | **String** |  | [optional] |
| **warehouse_name** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PublicDeliveryAppointmentStatusResponse.new(
  appointment_id: null,
  requested_date: null,
  status: null,
  time_slot: null,
  warehouse_name: null
)
```

