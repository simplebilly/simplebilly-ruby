# SimplebillyApi::Absence

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **absence_type** | [**AbsenceType**](AbsenceType.md) | One of \&quot;vacation\&quot;, \&quot;sick\&quot;, \&quot;sabbatical\&quot;, \&quot;parental\&quot;, \&quot;other\&quot;. | [optional] |
| **approved_at** | **Time** |  | [optional] |
| **approved_by** | **String** | References the user entity. | [optional] |
| **created_at** | **Time** |  | [optional] |
| **deleted_at** | **Time** |  | [optional] |
| **employee_id** | **String** | References the employee entity. | [optional] |
| **end_date** | **Date** |  | [optional] |
| **id** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **start_date** | **Date** |  | [optional] |
| **status** | [**AbsenceStatus**](AbsenceStatus.md) | One of \&quot;pending\&quot;, \&quot;approved\&quot;, \&quot;rejected\&quot;, \&quot;cancelled\&quot;. | [optional] |
| **tenant_id** | **String** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Absence.new(
  absence_type: null,
  approved_at: null,
  approved_by: null,
  created_at: null,
  deleted_at: null,
  employee_id: null,
  end_date: null,
  id: null,
  notes: null,
  start_date: null,
  status: null,
  tenant_id: null,
  updated_at: null
)
```

