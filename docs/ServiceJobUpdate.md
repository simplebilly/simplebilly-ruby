# SimplebillyApi::ServiceJobUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **String** | Street + zip + city of the job location. | [optional] |
| **customer_email** | **String** | Customer email for email notifications. | [optional] |
| **customer_id** | **String** | References the customer entity. | [optional] |
| **customer_name** | **String** | Denormalized customer name for quick display. | [optional] |
| **customer_phone** | **String** | Customer phone for SMS notifications later. | [optional] |
| **description** | **String** | What work needs to be done. | [optional] |
| **estimated_duration_minutes** | **Integer** | Estimated time for the job in minutes. | [optional] |
| **lat** | **Float** | Latitude for map display (OpenStreetMap). | [optional] |
| **lng** | **Float** | Longitude for map display (OpenStreetMap). | [optional] |
| **notes** | **String** |  | [optional] |
| **status** | [**ServiceJobStatus**](ServiceJobStatus.md) | Dispatch status: \&quot;pending\&quot;, \&quot;assigned\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot;, \&quot;cancelled\&quot;. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ServiceJobUpdate.new(
  address: null,
  customer_email: null,
  customer_id: null,
  customer_name: null,
  customer_phone: null,
  description: null,
  estimated_duration_minutes: null,
  lat: null,
  lng: null,
  notes: null,
  status: null
)
```

