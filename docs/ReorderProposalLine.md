# SimplebillyApi::ReorderProposalLine

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_stock** | **Integer** |  |  |
| **max_stock** | **Integer** |  | [optional] |
| **min_stock** | **Integer** |  | [optional] |
| **product_id** | **String** |  |  |
| **product_name** | **String** |  |  |
| **reorder_quantity** | **Integer** |  | [optional] |
| **sku** | **String** |  |  |
| **suggested_quantity** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReorderProposalLine.new(
  current_stock: null,
  max_stock: null,
  min_stock: null,
  product_id: null,
  product_name: null,
  reorder_quantity: null,
  sku: null,
  suggested_quantity: null
)
```

