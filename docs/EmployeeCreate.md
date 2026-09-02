# SimplebillyApi::EmployeeCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **String** |  | [optional] |
| **backup_employee_id** | **String** | References another employee who covers when this employee is absent. | [optional] |
| **bic** | **String** |  | [optional] |
| **city** | **String** |  | [optional] |
| **country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **date_of_birth** | **Date** |  | [optional] |
| **department_id** | **String** | References the department entity. | [optional] |
| **email** | **String** |  | [optional] |
| **first_name** | **String** |  | [optional] |
| **gender** | [**Gender**](Gender.md) | Gender for pay-transparency reporting: \&quot;male\&quot;, \&quot;female\&quot; or \&quot;diverse\&quot;. | [optional] |
| **hire_date** | **Date** |  | [optional] |
| **hourly_cost** | **String** | Hourly cost rate in EUR for labor-cost reporting; when unset the rate is derived from &#x60;monthly_salary / (weekly_hours * 4.33)&#x60;. | [optional] |
| **iban** | **String** |  | [optional] |
| **job_title** | **String** |  | [optional] |
| **last_login** | **Time** |  | [optional] |
| **last_name** | **String** |  | [optional] |
| **last_updated** | **Time** |  | [optional] |
| **monthly_salary** | **String** | Gross monthly salary in EUR for pay-transparency reporting. | [optional] |
| **phone** | **String** |  | [optional] |
| **state** | **String** |  | [optional] |
| **status** | [**EmployeeStatus**](EmployeeStatus.md) |  | [optional] |
| **user_id** | **String** | References the user entity. | [optional] |
| **weekly_hours** | **String** | Contractual weekly working hours for pay-transparency normalization. | [optional] |
| **zip** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EmployeeCreate.new(
  address: null,
  backup_employee_id: null,
  bic: null,
  city: null,
  country: null,
  date_of_birth: null,
  department_id: null,
  email: null,
  first_name: null,
  gender: null,
  hire_date: null,
  hourly_cost: null,
  iban: null,
  job_title: null,
  last_login: null,
  last_name: null,
  last_updated: null,
  monthly_salary: null,
  phone: null,
  state: null,
  status: null,
  user_id: null,
  weekly_hours: null,
  zip: null
)
```

