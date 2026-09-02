# SimplebillyApi::ProformaInvoiceCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **converted_at** | **Time** |  | [optional] |
| **converted_to_invoice_id** | **String** | Set when the proforma was converted into a real invoice. References the invoice entity. | [optional] |
| **currency** | [**CurrencyCode**](CurrencyCode.md) |  |  |
| **customer_id** | **String** | References the customer entity. | [optional] |
| **customer_snapshot** | **Object** | Snapshot of the recipient at issue time (address, VAT id, …). | [optional] |
| **issue_date** | **Date** |  |  |
| **line_items** | **Object** |  |  |
| **notes** | **String** |  | [optional] |
| **order_number** | **String** | Reference to the order/quote this proforma belongs to. | [optional] |
| **payment_due_date** | **Date** | Optional deadline the real invoice should carry after conversion. | [optional] |
| **quotation_id** | **String** | References the quotation entity. | [optional] |
| **status** | [**ProformaInvoiceStatus**](ProformaInvoiceStatus.md) | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. |  |
| **subtotal** | **String** |  |  |
| **total_amount** | **String** |  |  |
| **total_tax** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProformaInvoiceCreate.new(
  converted_at: null,
  converted_to_invoice_id: null,
  currency: null,
  customer_id: null,
  customer_snapshot: null,
  issue_date: null,
  line_items: null,
  notes: null,
  order_number: null,
  payment_due_date: null,
  quotation_id: null,
  status: null,
  subtotal: null,
  total_amount: null,
  total_tax: null
)
```

