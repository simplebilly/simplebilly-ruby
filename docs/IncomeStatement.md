# SimplebillyApi::IncomeStatement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **expense_items** | [**Array&lt;PnLItem&gt;**](PnLItem.md) |  |  |
| **net_income** | **String** |  |  |
| **revenue_items** | [**Array&lt;PnLItem&gt;**](PnLItem.md) |  |  |
| **total_expenses** | **String** |  |  |
| **total_revenue** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::IncomeStatement.new(
  expense_items: null,
  net_income: null,
  revenue_items: null,
  total_expenses: null,
  total_revenue: null
)
```

