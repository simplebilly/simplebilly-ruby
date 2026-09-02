# SimplebillyApi::BWAExpenses

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **expense_breakdown** | [**Array&lt;ExpenseItem&gt;**](ExpenseItem.md) |  |  |
| **total_expenses** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BWAExpenses.new(
  expense_breakdown: null,
  total_expenses: null
)
```

