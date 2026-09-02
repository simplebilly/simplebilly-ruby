# SimplebillyApi::ShippingCredentials

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **dhl** | [**DhlCredentials**](DhlCredentials.md) |  | [optional] |
| **ups** | [**UpsCredentials**](UpsCredentials.md) |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ShippingCredentials.new(
  dhl: null,
  ups: null
)
```

