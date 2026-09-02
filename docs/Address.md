# SimplebillyApi::Address

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **city** | **String** |  |  |
| **company** | **String** |  | [optional] |
| **country** | **String** | ISO 3166-1 alpha-2 country code (e.g. \&quot;DE\&quot;, \&quot;PL\&quot;, \&quot;FR\&quot;). |  |
| **email** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **phone** | **String** |  | [optional] |
| **street** | **String** |  |  |
| **street_number** | **String** |  |  |
| **zip** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Address.new(
  city: null,
  company: null,
  country: null,
  email: null,
  name: null,
  phone: null,
  street: null,
  street_number: null,
  zip: null
)
```

