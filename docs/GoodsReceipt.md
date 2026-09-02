# SimplebillyApi::GoodsReceipt

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gr_number** | **String** |  |  |
| **line_items** | **Object** | JSON array of &#x60;{product_id, name, quantity, batch_number?, expiry_date?, bin_location?}&#x60;. |  |
| **notes** | **String** |  | [optional] |
| **purchase_order_id** | **String** | References the purchase order entity. | [optional] |
| **receipt_date** | **Date** |  |  |
| **supplier_contact_id** | **String** | References the supplier entity. | [optional] |
| **supplier_name** | **String** |  | [optional] |
| **warehouse_id** | **String** | References the warehouse entity. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GoodsReceipt.new(
  gr_number: null,
  line_items: null,
  notes: null,
  purchase_order_id: null,
  receipt_date: null,
  supplier_contact_id: null,
  supplier_name: null,
  warehouse_id: null
)
```

