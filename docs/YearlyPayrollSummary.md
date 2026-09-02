# SimplebillyApi::YearlyPayrollSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **avg_employee_count** | **Integer** |  |  |
| **months** | [**Array&lt;PayrollSummaryItem&gt;**](PayrollSummaryItem.md) |  |  |
| **year** | **Integer** |  |  |
| **yearly_employer_cost** | **String** |  |  |
| **yearly_gross** | **String** |  |  |
| **yearly_net** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::YearlyPayrollSummary.new(
  avg_employee_count: null,
  months: null,
  year: null,
  yearly_employer_cost: null,
  yearly_gross: null,
  yearly_net: null
)
```

