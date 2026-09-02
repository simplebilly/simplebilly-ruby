# SimplebillyApi::AuthResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **access_token** | **String** |  | [optional] |
| **message** | **String** |  | [optional] |
| **refresh_token** | **String** |  | [optional] |
| **success** | **Boolean** |  |  |
| **user** | [**Model**](Model.md) |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AuthResponse.new(
  access_token: null,
  message: null,
  refresh_token: null,
  success: null,
  user: null
)
```

