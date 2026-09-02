# SimplebillyApi::JobPostingCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | **String** |  | [optional] |
| **department** | **String** |  | [optional] |
| **description** | **String** | What the job is; markdown/HTML. |  |
| **employment_type** | [**EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional] |
| **location** | **String** |  | [optional] |
| **remote** | **Boolean** |  |  |
| **required_skills** | **Object** | List of required skill names (JSON array of strings). |  |
| **requirements** | **String** | Structured profile of the required candidate (skills, experience). | [optional] |
| **salary_max** | **Integer** |  | [optional] |
| **salary_min** | **Integer** |  | [optional] |
| **status** | [**JobPostingStatus**](JobPostingStatus.md) | draft | published | closed |  |
| **title** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::JobPostingCreate.new(
  currency: null,
  department: null,
  description: null,
  employment_type: null,
  location: null,
  remote: null,
  required_skills: null,
  requirements: null,
  salary_max: null,
  salary_min: null,
  status: null,
  title: null
)
```

