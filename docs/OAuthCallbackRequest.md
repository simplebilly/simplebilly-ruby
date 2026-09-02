# SimplebillyApi::OAuthCallbackRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |
| **config** | **Object** |  | [optional] |
| **connection_id** | **String** |  | [optional] |
| **platform** | **String** |  |  |
| **shop_domain** | **String** |  | [optional] |
| **state** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::OAuthCallbackRequest.new(
  code: null,
  config: null,
  connection_id: null,
  platform: null,
  shop_domain: null,
  state: null
)
```

