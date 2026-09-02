# SimplebillyApi::PublicDeliveryAppointmentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** |  |  |
| **notes** | **String** |  | [optional] |
| **requested_date** | **Date** |  |  |
| **supplier_name** | **String** |  |  |
| **time_slot** | **String** |  | [optional] |
| **warehouse_code** | **String** | Warehouse &#x60;code&#x60; — the supplier does not know the warehouse uuid. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PublicDeliveryAppointmentRequest.new(
  email: null,
  notes: null,
  requested_date: null,
  supplier_name: null,
  time_slot: null,
  warehouse_code: null
)
```

