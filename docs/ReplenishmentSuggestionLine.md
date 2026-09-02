# SimplebillyApi::ReplenishmentSuggestionLine

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_stock** | **Integer** | Current stock in the target warehouse. |  |
| **max_stock** | **Integer** |  | [optional] |
| **min_stock** | **Integer** |  | [optional] |
| **product_id** | **String** |  |  |
| **product_name** | **String** |  |  |
| **sku** | **String** |  |  |
| **source_available** | **Integer** | Surplus available in the source warehouse (above its target). |  |
| **source_warehouse_id** | **String** |  |  |
| **suggested_quantity** | **Integer** |  |  |
| **target_warehouse_id** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReplenishmentSuggestionLine.new(
  current_stock: null,
  max_stock: null,
  min_stock: null,
  product_id: null,
  product_name: null,
  sku: null,
  source_available: null,
  source_warehouse_id: null,
  suggested_quantity: null,
  target_warehouse_id: null
)
```

