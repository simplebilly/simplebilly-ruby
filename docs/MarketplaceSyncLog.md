# SimplebillyApi::MarketplaceSyncLog

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **completed_at** | **Time** |  | [optional] |
| **connection_id** | **String** | References the marketplace connection entity. |  |
| **error_message** | **String** |  | [optional] |
| **items_failed** | **Integer** |  |  |
| **items_synced** | **Integer** |  |  |
| **platform** | **String** |  |  |
| **started_at** | **Time** |  |  |
| **status** | [**SyncLogStatus**](SyncLogStatus.md) |  |  |
| **sync_type** | [**SyncType**](SyncType.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::MarketplaceSyncLog.new(
  completed_at: null,
  connection_id: null,
  error_message: null,
  items_failed: null,
  items_synced: null,
  platform: null,
  started_at: null,
  status: null,
  sync_type: null
)
```

