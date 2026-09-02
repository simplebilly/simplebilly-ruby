# SimplebillyApi::LiquidityPosition

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **accounts_payable** | **Float** |  |  |
| **accounts_receivable** | **Float** |  |  |
| **cash_and_equivalents** | **Float** |  |  |
| **current_ratio** | **Float** |  |  |
| **quick_ratio** | **Float** |  |  |
| **working_capital** | **Float** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::LiquidityPosition.new(
  accounts_payable: null,
  accounts_receivable: null,
  cash_and_equivalents: null,
  current_ratio: null,
  quick_ratio: null,
  working_capital: null
)
```

