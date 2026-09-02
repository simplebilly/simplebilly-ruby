# SimplebillyApi::PaymentGatewayCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **config** | **Object** |  |  |
| **created_at** | **Time** |  |  |
| **deleted_at** | **Time** |  | [optional] |
| **enabled** | **Boolean** |  |  |
| **gateway_type** | [**GatewayType**](GatewayType.md) |  |  |
| **label** | **String** |  |  |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PaymentGatewayCreate.new(
  config: null,
  created_at: null,
  deleted_at: null,
  enabled: null,
  gateway_type: null,
  label: null,
  updated_at: null
)
```

