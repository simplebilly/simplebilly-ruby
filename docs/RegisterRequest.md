# SimplebillyApi::RegisterRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_name** | **String** |  |  |
| **email** | **String** |  |  |
| **first_name** | **String** |  |  |
| **last_name** | **String** |  |  |
| **password** | **String** |  |  |
| **privacy_accepted** | **Boolean** | GDPR consent — registration is rejected unless true. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::RegisterRequest.new(
  company_name: null,
  email: null,
  first_name: null,
  last_name: null,
  password: null,
  privacy_accepted: null
)
```

