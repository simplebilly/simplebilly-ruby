# SimplebillyApi::BWAReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **expenses** | [**BWAExpenses**](BWAExpenses.md) |  |  |
| **generated_at** | **String** |  |  |
| **period** | **String** |  |  |
| **revenue** | [**BWARevenue**](BWARevenue.md) |  |  |
| **summary** | [**BWASummary**](BWASummary.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BWAReport.new(
  expenses: null,
  generated_at: null,
  period: null,
  revenue: null,
  summary: null
)
```

