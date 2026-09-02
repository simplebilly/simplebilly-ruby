# SimplebillyApi::MethodSuitability

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **carrier** | **String** |  |  |
| **rate** | [**ShippingRate**](ShippingRate.md) |  | [optional] |
| **reasons** | **Array&lt;String&gt;** |  |  |
| **service** | **String** |  |  |
| **suitable** | **Boolean** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::MethodSuitability.new(
  carrier: null,
  rate: null,
  reasons: null,
  service: null,
  suitable: null
)
```

