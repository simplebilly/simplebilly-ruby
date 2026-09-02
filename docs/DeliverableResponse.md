# SimplebillyApi::DeliverableResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **available_stock** | **Integer** |  |  |
| **deliverable_quantity** | **Integer** |  |  |
| **max_sellable** | **Integer** |  | [optional] |
| **product_id** | **String** |  |  |
| **reserved_stock** | **Integer** |  |  |
| **warehouse_id** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DeliverableResponse.new(
  available_stock: null,
  deliverable_quantity: null,
  max_sellable: null,
  product_id: null,
  reserved_stock: null,
  warehouse_id: null
)
```

