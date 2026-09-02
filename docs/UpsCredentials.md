# SimplebillyApi::UpsCredentials

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **client_id** | **String** | OAuth 2.0 client credentials from developer.ups.com. |  |
| **client_secret** | **String** |  |  |
| **shipper_number** | **String** | UPS account number; required for label creation, optional for rates/tracking. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::UpsCredentials.new(
  client_id: null,
  client_secret: null,
  shipper_number: null
)
```

