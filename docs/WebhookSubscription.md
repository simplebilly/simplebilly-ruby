# SimplebillyApi::WebhookSubscription

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event_type** | **String** | Event type to react to (e.g. \&quot;order.created\&quot;); \&quot;*\&quot; &#x3D; all events. |  |
| **is_active** | **Boolean** |  | [optional] |
| **name** | **String** | Human label (e.g. \&quot;Warehouse app\&quot;). |  |
| **secret** | **String** | Shared secret for HMAC-SHA256 signature, sent as X-Signature. |  |
| **url** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::WebhookSubscription.new(
  event_type: null,
  is_active: null,
  name: null,
  secret: null,
  url: null
)
```

