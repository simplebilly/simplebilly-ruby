# SimplebillyApi::PayrollAutopayPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **debtor_bic** | **String** |  | [optional] |
| **debtor_iban** | **String** |  | [optional] |
| **debtor_name** | **String** |  | [optional] |
| **execution_date** | **Date** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayrollAutopayPayload.new(
  debtor_bic: null,
  debtor_iban: null,
  debtor_name: null,
  execution_date: null
)
```

