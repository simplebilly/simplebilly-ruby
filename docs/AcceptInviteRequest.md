# SimplebillyApi::AcceptInviteRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **first_name** | **String** |  |  |
| **last_name** | **String** |  |  |
| **password** | **String** |  |  |
| **privacy_accepted** | **Boolean** | GDPR consent — rejected unless true. |  |
| **token** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AcceptInviteRequest.new(
  first_name: null,
  last_name: null,
  password: null,
  privacy_accepted: null,
  token: null
)
```

