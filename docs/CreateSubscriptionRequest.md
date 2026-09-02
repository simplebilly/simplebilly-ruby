# SimplebillyApi::CreateSubscriptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event_type** | **String** |  |  |
| **is_active** | **Boolean** |  | [optional] |
| **name** | **String** |  |  |
| **secret** | **String** |  | [optional] |
| **url** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CreateSubscriptionRequest.new(
  event_type: null,
  is_active: null,
  name: null,
  secret: null,
  url: null
)
```

