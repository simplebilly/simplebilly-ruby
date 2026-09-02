# SimplebillyApi::Job

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attempts** | **Integer** |  | [optional] |
| **job_type** | **String** | Discriminator the worker dispatches on (e.g. \&quot;webhook.deliver\&quot;). |  |
| **max_attempts** | **Integer** |  |  |
| **payload** | **Object** |  | [optional] |
| **run_at** | **Time** | Earliest execution time; None &#x3D; run now. | [optional] |
| **status** | [**JobStatus**](JobStatus.md) | pending | running | done | failed |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Job.new(
  attempts: null,
  job_type: null,
  max_attempts: null,
  payload: null,
  run_at: null,
  status: null
)
```

