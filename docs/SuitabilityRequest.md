# SimplebillyApi::SuitabilityRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_annual_volume** | **Integer** |  | [optional] |
| **items** | [**Array&lt;CartItemInput&gt;**](CartItemInput.md) |  |  |
| **recipient** | [**Address**](Address.md) |  |  |
| **sender** | [**Address**](Address.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SuitabilityRequest.new(
  customer_annual_volume: null,
  items: null,
  recipient: null,
  sender: null
)
```

