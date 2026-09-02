# SimplebillyApi::TotpSetupResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **backup_codes** | **Array&lt;String&gt;** |  |  |
| **qr_code_url** | **String** |  |  |
| **secret** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TotpSetupResponse.new(
  backup_codes: null,
  qr_code_url: null,
  secret: null
)
```

