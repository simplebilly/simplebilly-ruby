# SimplebillyApi::StockMovement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delta** | **Integer** | Signed movement: positive &#x3D; into stock, negative &#x3D; out of stock. |  |
| **movement_type** | [**MovementType**](MovementType.md) | One of the &#x60;MOVEMENT_*&#x60; constants. |  |
| **product_id** | **String** | References the product entity. |  |
| **quantity** | **Integer** | Absolute quantity moved (always &gt;&#x3D; 0). |  |
| **reason** | **String** |  | [optional] |
| **reference_id** | **String** | Primary-key of the referencing entity. | [optional] |
| **reference_type** | [**ReferenceType**](ReferenceType.md) | Entity that caused the movement, e.g. &#x60;goods_receipt&#x60;, &#x60;stock_transfer&#x60;. | [optional] |
| **warehouse_id** | **String** | References the warehouse entity. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::StockMovement.new(
  delta: null,
  movement_type: null,
  product_id: null,
  quantity: null,
  reason: null,
  reference_id: null,
  reference_type: null,
  warehouse_id: null
)
```

