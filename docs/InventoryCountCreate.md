# SimplebillyApi::InventoryCountCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **count_date** | **Date** |  |  |
| **count_number** | **String** |  |  |
| **line_items** | **Object** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. |  |
| **notes** | **String** |  | [optional] |
| **status** | [**InventoryCountStatus**](InventoryCountStatus.md) | One of: draft | counting | reviewed | posted |  |
| **warehouse_id** | **String** | References the warehouse entity. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::InventoryCountCreate.new(
  count_date: null,
  count_number: null,
  line_items: null,
  notes: null,
  status: null,
  warehouse_id: null
)
```

