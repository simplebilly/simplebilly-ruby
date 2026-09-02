# SimplebillyApi::PublicDeliveryAppointmentResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **appointment_id** | **String** |  |  |
| **confirmation_hint** | **String** | Carries the status-check token (email is out of scope for now). |  |
| **message** | **String** |  |  |
| **status** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PublicDeliveryAppointmentResponse.new(
  appointment_id: null,
  confirmation_hint: null,
  message: null,
  status: null
)
```

