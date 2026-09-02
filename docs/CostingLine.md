# SimplebillyApi::CostingLine

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **line_cost** | **String** | total_quantity × unit_purchase_price (0 when price unknown). |  |
| **name** | **String** |  |  |
| **product_id** | **String** |  |  |
| **quantity_per_unit** | **Integer** | Component quantity required per finished unit. |  |
| **sku** | **String** |  |  |
| **total_quantity** | **Integer** | Total component quantity consumed by this order. |  |
| **unit_purchase_price** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CostingLine.new(
  line_cost: null,
  name: null,
  product_id: null,
  quantity_per_unit: null,
  sku: null,
  total_quantity: null,
  unit_purchase_price: null
)
```

