# SimplebillyApi::DatevBookingPreview

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_number** | **String** |  |  |
| **debit_credit** | **String** |  |  |
| **document_date** | **String** |  |  |
| **document_text** | **String** |  |  |
| **net_amount** | **String** |  |  |
| **opposite_account** | **String** |  |  |
| **tax_amount** | **String** |  | [optional] |
| **tax_rate** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DatevBookingPreview.new(
  account_number: null,
  debit_credit: null,
  document_date: null,
  document_text: null,
  net_amount: null,
  opposite_account: null,
  tax_amount: null,
  tax_rate: null
)
```

