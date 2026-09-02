# SimplebillyApi::CurrentInventoryValue

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **history** | [**Array&lt;InventoryValuePoint&gt;**](InventoryValuePoint.md) |  |  |
| **product_count** | **Integer** |  |  |
| **total_purchase_value** | **String** |  |  |
| **total_sales_value** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CurrentInventoryValue.new(
  history: null,
  product_count: null,
  total_purchase_value: null,
  total_sales_value: null
)
```

