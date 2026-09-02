# SimplebillyApi::ProductionOrderCosting

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cost_per_unit** | **String** | material_cost_total ÷ quantity. |  |
| **cost_source** | **String** | \&quot;actual\&quot; when costed from stock-movement consumption, else \&quot;planned\&quot;. |  |
| **lines** | [**Array&lt;CostingLine&gt;**](CostingLine.md) |  |  |
| **margin_per_unit** | **String** | sale_price − cost_per_unit. | [optional] |
| **margin_percent** | **String** | margin_per_unit ÷ cost_per_unit as a percentage. | [optional] |
| **material_cost_total** | **String** | Total material cost for the whole order. |  |
| **order_number** | **String** |  |  |
| **production_order_id** | **String** |  |  |
| **quantity** | **Integer** |  |  |
| **sale_price** | **String** | Finished product&#39;s sale price per unit (used to compute margin). | [optional] |
| **status** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProductionOrderCosting.new(
  cost_per_unit: null,
  cost_source: null,
  lines: null,
  margin_per_unit: null,
  margin_percent: null,
  material_cost_total: null,
  order_number: null,
  production_order_id: null,
  quantity: null,
  sale_price: null,
  status: null
)
```

