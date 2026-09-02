# SimplebillyApi::SupplierInvoiceCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | **String** |  | [optional] |
| **goods_receipt_id** | **String** | References the goods receipt entity. | [optional] |
| **invoice_date** | **Date** |  |  |
| **invoice_number** | **String** |  |  |
| **line_items** | **Object** | JSON array of &#x60;{product_id, name, quantity, unitPriceNet, taxRate}&#x60;. |  |
| **notes** | **String** |  | [optional] |
| **purchase_order_id** | **String** | References the purchase order entity. | [optional] |
| **status** | [**SupplierInvoiceStatus**](SupplierInvoiceStatus.md) | One of: draft | matched | has_variances | posted | cancelled |  |
| **supplier_contact_id** | **String** | References the supplier entity. | [optional] |
| **supplier_name** | **String** |  | [optional] |
| **total_gross_amount** | **String** |  | [optional] |
| **total_net_amount** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SupplierInvoiceCreate.new(
  currency: null,
  goods_receipt_id: null,
  invoice_date: null,
  invoice_number: null,
  line_items: null,
  notes: null,
  purchase_order_id: null,
  status: null,
  supplier_contact_id: null,
  supplier_name: null,
  total_gross_amount: null,
  total_net_amount: null
)
```

