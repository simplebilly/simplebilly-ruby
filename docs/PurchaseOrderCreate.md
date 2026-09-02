# SimplebillyApi::PurchaseOrderCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | **String** |  | [optional] |
| **delivery_address** | **Object** |  | [optional] |
| **expected_delivery_date** | **Date** |  | [optional] |
| **line_items** | **Object** | JSON array of &#x60;{product_id, name, quantity, unit_price_net, tax_rate, delivery_date}&#x60;. | [optional] |
| **notes** | **String** |  | [optional] |
| **order_date** | **Date** |  |  |
| **po_number** | **String** |  |  |
| **status** | [**PurchaseOrderStatus**](PurchaseOrderStatus.md) | One of: draft | ordered | partially_received | received | cancelled |  |
| **supplier_contact_id** | **String** | References the supplier entity. | [optional] |
| **supplier_name** | **String** |  | [optional] |
| **total_gross_amount** | **String** |  | [optional] |
| **total_net_amount** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PurchaseOrderCreate.new(
  currency: null,
  delivery_address: null,
  expected_delivery_date: null,
  line_items: null,
  notes: null,
  order_date: null,
  po_number: null,
  status: null,
  supplier_contact_id: null,
  supplier_name: null,
  total_gross_amount: null,
  total_net_amount: null
)
```

