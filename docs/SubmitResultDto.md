# SimplebillyApi::SubmitResultDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **answers** | **Array&lt;Integer&gt;** | Selected answer indices (required for scored builtin trainings). |  |
| **assignment_id** | **String** |  | [optional] |
| **score** | **Integer** | Score 0–100. Only trusted for plugin trainings without server-side scoring; builtin trainings are always re-scored from &#x60;answers&#x60;. |  |
| **training_code** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SubmitResultDto.new(
  answers: null,
  assignment_id: null,
  score: null,
  training_code: null
)
```

