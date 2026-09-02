# SimplebillyApi::ImportJobStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **String** | Set only when the job failed. | [optional] |
| **job_id** | **String** |  |  |
| **processed** | **Integer** |  |  |
| **progress** | **Integer** | 0–100 |  |
| **provider** | **String** | Which competitor the import came from (lexoffice | billbee); the frontend uses it to label the job. Absent for legacy jobs. | [optional] |
| **stage** | **String** | queued | fetching | downloading | importing | done |  |
| **status** | **String** | pending | running | done | failed |  |
| **total** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ImportJobStatus.new(
  error: null,
  job_id: null,
  processed: null,
  progress: null,
  provider: null,
  stage: null,
  status: null,
  total: null
)
```

