# SimplebillyApi::PayrollEntryApi

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **av_employee** | **String** |  |  |
| **av_employer** | **String** |  |  |
| **church_tax_amount** | **String** |  |  |
| **employee** | [**Employee**](Employee.md) |  | [optional] |
| **employee_id** | **String** |  |  |
| **entry_id** | **String** |  |  |
| **extra_payment_reason** | **String** |  | [optional] |
| **extra_payments** | **String** |  |  |
| **gross_salary** | **String** |  |  |
| **kv_employee** | **String** |  |  |
| **kv_employer** | **String** |  |  |
| **lohnsteuer** | **String** |  |  |
| **net_salary** | **String** |  |  |
| **notes** | **String** |  | [optional] |
| **pv_employee** | **String** |  |  |
| **pv_employer** | **String** |  |  |
| **run_id** | **String** |  |  |
| **rv_employee** | **String** |  |  |
| **rv_employer** | **String** |  |  |
| **sick_days** | **Integer** |  |  |
| **soli** | **String** |  |  |
| **status** | [**PayrollRunStatus**](PayrollRunStatus.md) |  |  |
| **total_deductions** | **String** |  |  |
| **total_employer_cost** | **String** |  |  |
| **vacation_days_used** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayrollEntryApi.new(
  av_employee: null,
  av_employer: null,
  church_tax_amount: null,
  employee: null,
  employee_id: null,
  entry_id: null,
  extra_payment_reason: null,
  extra_payments: null,
  gross_salary: null,
  kv_employee: null,
  kv_employer: null,
  lohnsteuer: null,
  net_salary: null,
  notes: null,
  pv_employee: null,
  pv_employer: null,
  run_id: null,
  rv_employee: null,
  rv_employer: null,
  sick_days: null,
  soli: null,
  status: null,
  total_deductions: null,
  total_employer_cost: null,
  vacation_days_used: null
)
```

