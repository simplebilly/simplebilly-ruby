# SimplebillyApi::ShippingThreshold

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **is_active** | **Boolean** |  | [optional] |
| **max_sellable** | **Integer** | Optional ceiling for the deliverable quantity. | [optional] |
| **name** | **String** |  |  |
| **notes** | **String** |  | [optional] |
| **product_id** | **String** | None &#x3D; applies to all products. References the product entity. | [optional] |
| **reserve_stock** | **Integer** | Buffer of stock that must not be sold. | [optional] |
| **warehouse_id** | **String** | None &#x3D; applies to all warehouses. References the warehouse entity. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ShippingThreshold.new(
  is_active: null,
  max_sellable: null,
  name: null,
  notes: null,
  product_id: null,
  reserve_stock: null,
  warehouse_id: null
)
```

