# SimplebillyApi::SubmitResultResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **certificate_id** | **String** |  | [optional] |
| **completion_id** | **String** |  |  |
| **pass_score** | **Integer** |  |  |
| **passed** | **Boolean** |  |  |
| **score** | **Integer** |  |  |
| **valid_until** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SubmitResultResponse.new(
  certificate_id: null,
  completion_id: null,
  pass_score: null,
  passed: null,
  score: null,
  valid_until: null
)
```

