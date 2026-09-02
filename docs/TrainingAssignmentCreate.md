# SimplebillyApi::TrainingAssignmentCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **assigned_by** | **String** |  | [optional] |
| **due_date** | **Date** |  | [optional] |
| **employee_id** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **status** | [**AssignmentStatus**](AssignmentStatus.md) |  | [optional] |
| **training_id** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TrainingAssignmentCreate.new(
  assigned_by: null,
  due_date: null,
  employee_id: null,
  notes: null,
  status: null,
  training_id: null
)
```

