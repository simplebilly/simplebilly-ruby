# SimplebillyApi::TenantUser

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** |  |  |
| **email_verified** | **Boolean** |  |  |
| **is_active** | **Boolean** |  |  |
| **joined_at** | **Time** |  |  |
| **last_login** | **Time** |  | [optional] |
| **name** | **String** |  |  |
| **permissions** | **Array&lt;String&gt;** |  |  |
| **role** | **String** |  |  |
| **user_id** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TenantUser.new(
  email: null,
  email_verified: null,
  is_active: null,
  joined_at: null,
  last_login: null,
  name: null,
  permissions: null,
  role: null,
  user_id: null
)
```

