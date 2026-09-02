# SimplebillyApi::PayrollRunApi

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **approved_at** | **Time** |  | [optional] |
| **approved_by** | **String** |  | [optional] |
| **created_at** | **Time** |  |  |
| **entries** | [**Array&lt;PayrollEntryApi&gt;**](PayrollEntryApi.md) |  |  |
| **month** | **Integer** |  |  |
| **payment_date** | **Date** |  | [optional] |
| **period_label** | **String** |  |  |
| **run_id** | **String** |  |  |
| **status** | [**PayrollRunStatus**](PayrollRunStatus.md) |  |  |
| **tenant_id** | **String** |  |  |
| **total_employee_count** | **Integer** |  |  |
| **total_employer_cost** | **String** |  |  |
| **total_gross** | **String** |  |  |
| **total_net** | **String** |  |  |
| **total_social_security** | **String** |  |  |
| **total_taxes** | **String** |  |  |
| **updated_at** | **Time** |  | [optional] |
| **year** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayrollRunApi.new(
  approved_at: null,
  approved_by: null,
  created_at: null,
  entries: null,
  month: null,
  payment_date: null,
  period_label: null,
  run_id: null,
  status: null,
  tenant_id: null,
  total_employee_count: null,
  total_employer_cost: null,
  total_gross: null,
  total_net: null,
  total_social_security: null,
  total_taxes: null,
  updated_at: null,
  year: null
)
```

