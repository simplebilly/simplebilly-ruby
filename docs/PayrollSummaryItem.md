# SimplebillyApi::PayrollSummaryItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **employee_count** | **Integer** |  |  |
| **month** | **String** |  |  |
| **status** | [**PayrollRunStatus**](PayrollRunStatus.md) |  |  |
| **total_employer_cost** | **String** |  |  |
| **total_gross** | **String** |  |  |
| **total_net** | **String** |  |  |
| **year** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayrollSummaryItem.new(
  employee_count: null,
  month: null,
  status: null,
  total_employer_cost: null,
  total_gross: null,
  total_net: null,
  year: null
)
```

