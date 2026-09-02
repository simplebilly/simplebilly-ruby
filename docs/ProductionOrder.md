# SimplebillyApi::ProductionOrder

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bom_id** | **String** | References the BOM entity. | [optional] |
| **components** | **Object** | JSON snapshot of the BOM components at creation time. | [optional] |
| **end_date** | **Date** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **order_number** | **String** |  |  |
| **product_id** | **String** | The finished product to manufacture. References the product entity. |  |
| **quantity** | **Integer** | Quantity of finished product to produce. |  |
| **source_warehouse_id** | **String** | Warehouse components are consumed from. References the warehouse entity. | [optional] |
| **start_date** | **Date** |  | [optional] |
| **status** | [**ProductionOrderStatus**](ProductionOrderStatus.md) | One of: planned | in_production | completed | cancelled | [optional] |
| **target_warehouse_id** | **String** | Warehouse the finished product is added to. References the warehouse entity. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProductionOrder.new(
  bom_id: null,
  components: null,
  end_date: null,
  notes: null,
  order_number: null,
  product_id: null,
  quantity: null,
  source_warehouse_id: null,
  start_date: null,
  status: null,
  target_warehouse_id: null
)
```

