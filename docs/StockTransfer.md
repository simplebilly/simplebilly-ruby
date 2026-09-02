# SimplebillyApi::StockTransfer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **line_items** | **Object** | JSON array of &#x60;{product_id, name, quantity, batch_number?}&#x60;. |  |
| **notes** | **String** |  | [optional] |
| **source_warehouse_id** | **String** | References the warehouse entity. |  |
| **status** | [**StockTransferStatus**](StockTransferStatus.md) | One of: draft | completed | cancelled |  |
| **target_warehouse_id** | **String** | References the warehouse entity. |  |
| **transfer_date** | **Date** |  |  |
| **transfer_number** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::StockTransfer.new(
  line_items: null,
  notes: null,
  source_warehouse_id: null,
  status: null,
  target_warehouse_id: null,
  transfer_date: null,
  transfer_number: null
)
```

