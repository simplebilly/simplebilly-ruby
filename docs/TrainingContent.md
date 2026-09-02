# SimplebillyApi::TrainingContent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |
| **contact** | [**ContactInfo**](ContactInfo.md) |  |  |
| **pass_score** | **Integer** |  |  |
| **quiz** | [**Array&lt;QuizQuestion&gt;**](QuizQuestion.md) |  |  |
| **sections** | [**Array&lt;Section&gt;**](Section.md) |  |  |
| **title** | **String** |  |  |
| **title_en** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TrainingContent.new(
  code: null,
  contact: null,
  pass_score: null,
  quiz: null,
  sections: null,
  title: null,
  title_en: null
)
```

