# SimplebillyApi::MarketplaceWebhookEvent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** | References the marketplace connection entity. |  |
| **event_body** | **Object** |  | [optional] |
| **event_type** | **String** |  |  |
| **headers** | **Object** |  | [optional] |
| **platform** | **String** |  |  |
| **processed** | **Boolean** |  | [optional] |
| **processing_error** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::MarketplaceWebhookEvent.new(
  connection_id: null,
  event_body: null,
  event_type: null,
  headers: null,
  platform: null,
  processed: null,
  processing_error: null
)
```

