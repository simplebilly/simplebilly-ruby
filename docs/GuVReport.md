# SimplebillyApi::GuVReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **expenses** | [**Array&lt;GuVItem&gt;**](GuVItem.md) |  |  |
| **generated_at** | **String** |  |  |
| **net_income** | **String** |  |  |
| **period** | **String** |  |  |
| **revenue** | [**Array&lt;GuVItem&gt;**](GuVItem.md) |  |  |
| **total_expenses** | **String** |  |  |
| **total_revenue** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GuVReport.new(
  expenses: null,
  generated_at: null,
  net_income: null,
  period: null,
  revenue: null,
  total_expenses: null,
  total_revenue: null
)
```

