# SimplebillyApi::Quotation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **Object** |  | [optional] |
| **contact_id** | **String** | References the contact entity. | [optional] |
| **contact_name** | **String** |  | [optional] |
| **currency** | **String** |  |  |
| **expiration_date** | **Date** |  | [optional] |
| **files** | **Object** |  | [optional] |
| **introduction** | **String** |  | [optional] |
| **line_items** | **Object** |  | [optional] |
| **preceding_sales_voucher_id** | **String** | References the preceding sales voucher entity. | [optional] |
| **preceding_sales_voucher_type** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] |
| **quotation_number** | **String** |  | [optional] |
| **remark** | **String** |  | [optional] |
| **subtotal** | **String** |  | [optional] |
| **tax_condition** | **String** |  | [optional] |
| **title** | **String** |  | [optional] |
| **total_amount** | **String** |  | [optional] |
| **total_tax** | **String** |  | [optional] |
| **voucher_date** | **Date** |  |  |
| **voucher_status** | [**VoucherStatus**](VoucherStatus.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Quotation.new(
  address: null,
  contact_id: null,
  contact_name: null,
  currency: null,
  expiration_date: null,
  files: null,
  introduction: null,
  line_items: null,
  preceding_sales_voucher_id: null,
  preceding_sales_voucher_type: null,
  quotation_number: null,
  remark: null,
  subtotal: null,
  tax_condition: null,
  title: null,
  total_amount: null,
  total_tax: null,
  voucher_date: null,
  voucher_status: null
)
```

