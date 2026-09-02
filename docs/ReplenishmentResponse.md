# SimplebillyApi::ReplenishmentResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **generated_at** | **Time** |  |  |
| **lines** | [**Array&lt;ReplenishmentSuggestionLine&gt;**](ReplenishmentSuggestionLine.md) |  |  |
| **target_warehouse_id** | **String** |  |  |
| **total_suggested_quantity** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReplenishmentResponse.new(
  generated_at: null,
  lines: null,
  target_warehouse_id: null,
  total_suggested_quantity: null
)
```

