# SimplebillyApi::LoginRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** |  |  |
| **password** | **String** |  |  |
| **totp_code** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::LoginRequest.new(
  email: null,
  password: null,
  totp_code: null
)
```

