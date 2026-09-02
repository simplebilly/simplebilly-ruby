# SimplebillyApi::PaymentGatewayUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **config** | **Object** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **deleted_at** | **Time** |  | [optional] |
| **enabled** | **Boolean** |  | [optional] |
| **gateway_type** | [**GatewayType**](GatewayType.md) |  | [optional] |
| **label** | **String** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PaymentGatewayUpdate.new(
  config: null,
  created_at: null,
  deleted_at: null,
  enabled: null,
  gateway_type: null,
  label: null,
  updated_at: null
)
```

