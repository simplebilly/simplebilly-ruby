# SimplebillyApi::Model

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **backup_codes** | **Array&lt;String&gt;** |  |  |
| **created_at** | **Time** |  |  |
| **deleted_at** | **Time** |  | [optional] |
| **email** | **String** |  |  |
| **email_verified** | **Boolean** |  |  |
| **id** | **String** |  |  |
| **is_active** | **Boolean** |  |  |
| **is_totp_enabled** | **Boolean** |  |  |
| **last_login** | **Time** |  | [optional] |
| **name** | **String** |  |  |
| **oauth_id** | **String** |  | [optional] |
| **oauth_provider** | **String** |  | [optional] |
| **password_changed_at** | **Time** | Set on password change; auth/refresh tokens issued before this timestamp are rejected by the auth middleware. | [optional] |
| **password_hash** | **String** |  |  |
| **picture** | **String** |  | [optional] |
| **privacy_accepted_at** | **Time** | When the user accepted the data privacy policy (GDPR consent record). | [optional] |
| **totp_secret** | **String** |  | [optional] |
| **updated_at** | **Time** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Model.new(
  backup_codes: null,
  created_at: null,
  deleted_at: null,
  email: null,
  email_verified: null,
  id: null,
  is_active: null,
  is_totp_enabled: null,
  last_login: null,
  name: null,
  oauth_id: null,
  oauth_provider: null,
  password_changed_at: null,
  password_hash: null,
  picture: null,
  privacy_accepted_at: null,
  totp_secret: null,
  updated_at: null
)
```

