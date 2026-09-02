# SimplebillyApi::TrainingAssignment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **assigned_by** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **deleted_at** | **Time** |  | [optional] |
| **due_date** | **Date** |  | [optional] |
| **employee_id** | **String** |  | [optional] |
| **id** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **status** | [**AssignmentStatus**](AssignmentStatus.md) |  | [optional] |
| **tenant_id** | **String** |  | [optional] |
| **training_id** | **String** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TrainingAssignment.new(
  assigned_by: null,
  created_at: null,
  deleted_at: null,
  due_date: null,
  employee_id: null,
  id: null,
  notes: null,
  status: null,
  tenant_id: null,
  training_id: null,
  updated_at: null
)
```

