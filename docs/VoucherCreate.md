# SimplebillyApi::VoucherCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  | [optional] |
| **contact_id** | **String** | References the contact entity. | [optional] |
| **contact_name** | **String** |  | [optional] |
| **currency** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **file_attachments** | **Object** |  | [optional] |
| **line_items** | **Object** |  | [optional] |
| **metadata** | **Object** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **open_amount** | **String** |  | [optional] |
| **paid_date** | **Date** |  | [optional] |
| **payment_status** | [**PaymentStatus**](PaymentStatus.md) |  | [optional] |
| **tax_amounts** | **Object** |  | [optional] |
| **tax_condition** | **String** |  | [optional] |
| **total_gross_amount** | **String** |  | [optional] |
| **total_net_amount** | **String** |  | [optional] |
| **voucher_date** | **Date** |  |  |
| **voucher_number** | **String** |  | [optional] |
| **voucher_status** | [**VoucherStatus**](VoucherStatus.md) |  |  |
| **voucher_type** | [**VoucherType**](VoucherType.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::VoucherCreate.new(
  category_id: null,
  contact_id: null,
  contact_name: null,
  currency: null,
  description: null,
  file_attachments: null,
  line_items: null,
  metadata: null,
  notes: null,
  open_amount: null,
  paid_date: null,
  payment_status: null,
  tax_amounts: null,
  tax_condition: null,
  total_gross_amount: null,
  total_net_amount: null,
  voucher_date: null,
  voucher_number: null,
  voucher_status: null,
  voucher_type: null
)
```

