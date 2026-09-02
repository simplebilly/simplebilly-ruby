# SimplebillyApi::JobApplication

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cv_file** | **String** | Relative path of the stored CV file under the upload dir. | [optional] |
| **cv_text** | **String** | Extracted CV text, used for match-scoring. | [optional] |
| **email** | **String** |  | [optional] |
| **match_reason** | **String** |  | [optional] |
| **match_score** | **Integer** | 0-100 LLM match score against the posting&#39;s required profile. | [optional] |
| **name** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **posting_id** | **String** | References the job_posting entity. | [optional] |
| **source** | **String** | website | email | board |  |
| **status** | [**ApplicationStatus**](ApplicationStatus.md) | new | reviewing | interview | hired | rejected |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::JobApplication.new(
  cv_file: null,
  cv_text: null,
  email: null,
  match_reason: null,
  match_score: null,
  name: null,
  phone: null,
  posting_id: null,
  source: null,
  status: null
)
```

