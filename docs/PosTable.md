# SimplebillyApi::PosTable

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_order_number** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **status** | [**PosTableStatus**](PosTableStatus.md) |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PosTable.new(
  current_order_number: null,
  name: null,
  status: null
)
```

