# SimplebillyApi::CreateShipmentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **carrier** | **String** | Carrier name as configured in shipping settings: &#x60;ups&#x60; or &#x60;dhl&#x60;. |  |
| **service** | **String** |  | [optional] |
| **weight_kg** | **Float** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CreateShipmentRequest.new(
  carrier: null,
  service: null,
  weight_kg: null
)
```

