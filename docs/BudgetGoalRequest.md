# SimplebillyApi::BudgetGoalRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_goal** | **String** | Monthly goal amount (gross). 0 means \&quot;no goal\&quot; (fallback to default). |  |
| **year** | **Integer** | Budget year the goal applies to. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BudgetGoalRequest.new(
  monthly_goal: null,
  year: null
)
```

