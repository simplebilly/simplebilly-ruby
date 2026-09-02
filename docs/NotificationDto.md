# SimplebillyApi::NotificationDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created_at** | **Time** |  |  |
| **id** | **String** |  |  |
| **is_read** | **Boolean** |  |  |
| **message** | **String** |  | [optional] |
| **sent_via_email** | **Boolean** |  |  |
| **tenant_id** | **String** |  |  |
| **title** | **String** |  |  |
| **user_id** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::NotificationDto.new(
  created_at: null,
  id: null,
  is_read: null,
  message: null,
  sent_via_email: null,
  tenant_id: null,
  title: null,
  user_id: null
)
```

