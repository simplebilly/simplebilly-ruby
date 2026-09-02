# SimplebillyApi::PayrollSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **first_name** | **String** |  |  |
| **hourly_gross** | **String** |  | [optional] |
| **id** | **String** |  |  |
| **job_title** | **String** |  |  |
| **last_name** | **String** |  |  |
| **monthly_salary** | **String** |  | [optional] |
| **months** | [**Array&lt;PayrollMonth&gt;**](PayrollMonth.md) |  |  |
| **weekly_hours** | **String** |  | [optional] |
| **year** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayrollSummary.new(
  first_name: null,
  hourly_gross: null,
  id: null,
  job_title: null,
  last_name: null,
  monthly_salary: null,
  months: null,
  weekly_hours: null,
  year: null
)
```

