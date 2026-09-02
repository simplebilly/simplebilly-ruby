# SimplebillyApi::SmtpConfig

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **encryption** | [**SmtpEncryption**](SmtpEncryption.md) |  |  |
| **from_address** | **String** |  |  |
| **from_name** | **String** |  | [optional] |
| **host** | **String** |  |  |
| **password** | **String** |  |  |
| **port** | **Integer** |  |  |
| **timeout_seconds** | **Integer** |  | [optional] |
| **username** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SmtpConfig.new(
  encryption: null,
  from_address: null,
  from_name: null,
  host: null,
  password: null,
  port: null,
  timeout_seconds: null,
  username: null
)
```

