# SimplebillyApi::DeliveryNoteCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **Object** |  | [optional] |
| **contact_id** | **String** | References the contact entity. | [optional] |
| **contact_name** | **String** |  | [optional] |
| **currency** | **String** |  |  |
| **delivery_date** | **Date** |  | [optional] |
| **delivery_note_number** | **String** |  | [optional] |
| **files** | **Object** |  | [optional] |
| **introduction** | **String** |  | [optional] |
| **line_items** | **Object** |  | [optional] |
| **preceding_sales_voucher_id** | **String** | References the preceding sales voucher entity. | [optional] |
| **preceding_sales_voucher_type** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] |
| **remark** | **String** |  | [optional] |
| **shipping_date** | **Date** |  | [optional] |
| **shipping_method** | **String** |  | [optional] |
| **title** | **String** |  | [optional] |
| **voucher_date** | **Date** |  |  |
| **voucher_status** | [**VoucherStatus**](VoucherStatus.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DeliveryNoteCreate.new(
  address: null,
  contact_id: null,
  contact_name: null,
  currency: null,
  delivery_date: null,
  delivery_note_number: null,
  files: null,
  introduction: null,
  line_items: null,
  preceding_sales_voucher_id: null,
  preceding_sales_voucher_type: null,
  remark: null,
  shipping_date: null,
  shipping_method: null,
  title: null,
  voucher_date: null,
  voucher_status: null
)
```

