# SimplebillyApi::SyncLog

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **completed_at** | **Time** |  | [optional] |
| **connection_id** | **String** |  |  |
| **error_message** | **String** |  | [optional] |
| **items_failed** | **Integer** |  |  |
| **items_synced** | **Integer** |  |  |
| **log_id** | **String** |  |  |
| **platform** | **String** |  |  |
| **started_at** | **Time** |  |  |
| **status** | **String** |  |  |
| **sync_type** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SyncLog.new(
  completed_at: null,
  connection_id: null,
  error_message: null,
  items_failed: null,
  items_synced: null,
  log_id: null,
  platform: null,
  started_at: null,
  status: null,
  sync_type: null
)
```

