# SimplebillyApi::DownPaymentInvoice

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  | [optional] |
| **contact_name** | **String** |  | [optional] |
| **created_at** | **String** |  | [readonly] |
| **currency** | **String** |  |  |
| **id** | **String** |  |  |
| **notes** | **String** |  | [optional] |
| **paid_amount** | **String** |  |  |
| **total_amount** | **String** |  |  |
| **voucher_date** | **Date** |  |  |
| **voucher_number** | **String** |  | [optional] |
| **voucher_status** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DownPaymentInvoice.new(
  contact_id: null,
  contact_name: null,
  created_at: null,
  currency: null,
  id: null,
  notes: null,
  paid_amount: null,
  total_amount: null,
  voucher_date: null,
  voucher_number: null,
  voucher_status: null
)
```

