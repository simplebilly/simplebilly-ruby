# SimplebillyApi::DeliveryAppointment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** |  |  |
| **notes** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **requested_date** | **Date** |  |  |
| **status** | [**DeliveryAppointmentStatus**](DeliveryAppointmentStatus.md) | One of: requested | confirmed | arrived | cancelled | completed |  |
| **supplier_name** | **String** |  |  |
| **time_slot** | **String** | e.g. \&quot;08:00-10:00\&quot; | [optional] |
| **warehouse_id** | **String** | References the warehouse entity. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DeliveryAppointment.new(
  email: null,
  notes: null,
  phone: null,
  requested_date: null,
  status: null,
  supplier_name: null,
  time_slot: null,
  warehouse_id: null
)
```

