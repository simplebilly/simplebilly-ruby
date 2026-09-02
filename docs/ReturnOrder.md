# SimplebillyApi::ReturnOrder

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_contact_id** | **String** | References the contact entity. | [optional] |
| **customer_name** | **String** |  | [optional] |
| **line_items** | **Object** | JSON array of &#x60;{product_id, name, quantity, condition, restock, batch_number?}&#x60;. | [optional] |
| **notes** | **String** |  | [optional] |
| **order_id** | **String** | References the order entity. | [optional] |
| **order_number** | **String** |  | [optional] |
| **return_number** | **String** |  |  |
| **return_reason** | **String** |  | [optional] |
| **status** | [**ReturnOrderStatus**](ReturnOrderStatus.md) | One of: requested | received | inspected | restocked | closed |  |
| **warehouse_id** | **String** | Warehouse into which restockable items are returned. References the warehouse entity. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReturnOrder.new(
  customer_contact_id: null,
  customer_name: null,
  line_items: null,
  notes: null,
  order_id: null,
  order_number: null,
  return_number: null,
  return_reason: null,
  status: null,
  warehouse_id: null
)
```

