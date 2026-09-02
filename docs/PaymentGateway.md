# SimplebillyApi::PaymentGateway

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **config** | **Object** |  |  |
| **created_at** | **Time** |  |  |
| **deleted_at** | **Time** |  | [optional] |
| **enabled** | **Boolean** |  |  |
| **gateway_id** | **String** |  |  |
| **gateway_type** | [**GatewayType**](GatewayType.md) |  |  |
| **label** | **String** |  |  |
| **tenant_id** | **String** |  |  |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PaymentGateway.new(
  config: null,
  created_at: null,
  deleted_at: null,
  enabled: null,
  gateway_id: null,
  gateway_type: null,
  label: null,
  tenant_id: null,
  updated_at: null
)
```

