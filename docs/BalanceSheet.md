# SimplebillyApi::BalanceSheet

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **assets** | [**Array&lt;BalanceItem&gt;**](BalanceItem.md) |  |  |
| **balanced** | **Boolean** |  |  |
| **equity_liabilities** | [**Array&lt;BalanceItem&gt;**](BalanceItem.md) |  |  |
| **total_assets** | **String** |  |  |
| **total_equity_liabilities** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BalanceSheet.new(
  assets: null,
  balanced: null,
  equity_liabilities: null,
  total_assets: null,
  total_equity_liabilities: null
)
```

