# SimplebillyApi::DhlCredentials

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_key** | **String** | DHL-API-Key from developer.dhl.com (required for tracking). |  |
| **client_id** | **String** | Client credentials from the DHL developer app; required for label creation. | [optional] |
| **client_secret** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DhlCredentials.new(
  api_key: null,
  client_id: null,
  client_secret: null
)
```

