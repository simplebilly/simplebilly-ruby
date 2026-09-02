# SimplebillyApi::OAuthAuthorizeRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **config** | **Object** | Optional platform-specific config (e.g. Shopify &#x60;shop_domain&#x60;, &#x60;api_key&#x60;, &#x60;api_secret&#x60;) needed to build the authorization URL. | [optional] |
| **platform** | **String** |  |  |
| **redirect_uri** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::OAuthAuthorizeRequest.new(
  config: null,
  platform: null,
  redirect_uri: null
)
```

