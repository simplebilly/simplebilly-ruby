# SimplebillyApi::MyTrainingItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **assignment_id** | **String** |  |  |
| **certificate_id** | **String** |  | [optional] |
| **code** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **due_date** | **Date** |  | [optional] |
| **last_score** | **Integer** |  | [optional] |
| **pass_score** | **Integer** |  |  |
| **passed** | **Boolean** |  | [optional] |
| **status** | [**AssignmentStatus**](AssignmentStatus.md) |  |  |
| **title** | **String** |  |  |
| **training_id** | **String** |  |  |
| **valid_until** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::MyTrainingItem.new(
  assignment_id: null,
  certificate_id: null,
  code: null,
  description: null,
  due_date: null,
  last_score: null,
  pass_score: null,
  passed: null,
  status: null,
  title: null,
  training_id: null,
  valid_until: null
)
```

