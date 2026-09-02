# SimplebillyApi::ServiceAssignmentUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **employee_id** | **String** | References the employees entity. | [optional] |
| **job_id** | **String** | References the service_jobs entity. | [optional] |
| **notes** | **String** |  | [optional] |
| **scheduled_date** | **Date** | Work day the assignment is scheduled for. | [optional] |
| **scheduled_end** | **String** | Planned end time of the assignment. | [optional] |
| **scheduled_start** | **String** | Planned start time of the assignment. | [optional] |
| **status** | [**ServiceAssignmentStatus**](ServiceAssignmentStatus.md) | Assignment lifecycle status: \&quot;planned\&quot;, \&quot;confirmed\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot; or \&quot;cancelled\&quot;. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ServiceAssignmentUpdate.new(
  employee_id: null,
  job_id: null,
  notes: null,
  scheduled_date: null,
  scheduled_end: null,
  scheduled_start: null,
  status: null
)
```

