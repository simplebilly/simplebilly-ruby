# SimplebillyApi::PosTableCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_order_number** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **status** | [**PosTableStatus**](PosTableStatus.md) |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PosTableCreate.new(
  current_order_number: null,
  name: null,
  status: null
)
```

