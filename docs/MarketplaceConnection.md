# SimplebillyApi::MarketplaceConnection

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **config** | **Object** |  |  |
| **connection_id** | **String** |  |  |
| **connector_type** | [**ConnectorType**](ConnectorType.md) |  |  |
| **created_at** | **Time** |  |  |
| **is_active** | **Boolean** |  |  |
| **label** | **String** |  |  |
| **last_sync_at** | **Time** |  | [optional] |
| **platform** | **String** |  |  |
| **platform_user_id** | **String** |  | [optional] |
| **scopes** | **String** |  | [optional] |
| **shop_domain** | **String** |  | [optional] |
| **shop_name** | **String** |  | [optional] |
| **sync_status** | **String** |  | [optional] |
| **tenant_id** | **String** |  |  |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::MarketplaceConnection.new(
  config: null,
  connection_id: null,
  connector_type: null,
  created_at: null,
  is_active: null,
  label: null,
  last_sync_at: null,
  platform: null,
  platform_user_id: null,
  scopes: null,
  shop_domain: null,
  shop_name: null,
  sync_status: null,
  tenant_id: null,
  updated_at: null
)
```

