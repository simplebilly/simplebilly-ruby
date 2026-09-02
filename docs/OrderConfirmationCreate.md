# SimplebillyApi::OrderConfirmationCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **Object** |  | [optional] |
| **confirmation_number** | **String** |  | [optional] |
| **contact_id** | **String** | References the contact entity. | [optional] |
| **contact_name** | **String** |  | [optional] |
| **currency** | **String** |  |  |
| **files** | **Object** |  | [optional] |
| **introduction** | **String** |  | [optional] |
| **line_items** | **Object** |  | [optional] |
| **preceding_sales_voucher_id** | **String** | References the preceding sales voucher entity. | [optional] |
| **preceding_sales_voucher_type** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] |
| **remark** | **String** |  | [optional] |
| **tax_condition** | **String** |  | [optional] |
| **title** | **String** |  | [optional] |
| **voucher_date** | **Date** |  |  |
| **voucher_status** | [**VoucherStatus**](VoucherStatus.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::OrderConfirmationCreate.new(
  address: null,
  confirmation_number: null,
  contact_id: null,
  contact_name: null,
  currency: null,
  files: null,
  introduction: null,
  line_items: null,
  preceding_sales_voucher_id: null,
  preceding_sales_voucher_type: null,
  remark: null,
  tax_condition: null,
  title: null,
  voucher_date: null,
  voucher_status: null
)
```

