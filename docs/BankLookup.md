# SimplebillyApi::BankLookup

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bank_name** | **String** |  | [optional] |
| **bic** | **String** |  | [optional] |
| **iban** | **String** |  |  |
| **nextgenpsd2_url** | **String** |  | [optional] |
| **psd2_supported** | **Boolean** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BankLookup.new(
  bank_name: null,
  bic: null,
  iban: null,
  nextgenpsd2_url: null,
  psd2_supported: null
)
```

