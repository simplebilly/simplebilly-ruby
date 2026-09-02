# SimplebillyApi::GdprRefreshToken

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created_at** | **Time** |  |  |
| **expires_at** | **Time** |  |  |
| **id** | **String** |  |  |
| **revoked_at** | **Time** |  | [optional] |
| **tenant_id** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GdprRefreshToken.new(
  created_at: null,
  expires_at: null,
  id: null,
  revoked_at: null,
  tenant_id: null
)
```

