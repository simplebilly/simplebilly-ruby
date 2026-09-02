# SimplebillyApi::PriceTier

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_group_id** | **String** | None &#x3D; tier applies to all customers; otherwise a customer group id. | [optional] |
| **min_quantity** | **Integer** | Quantity from which this tier applies (inclusive). | [optional] |
| **product_id** | **String** | References the product entity. |  |
| **unit_price** | **String** | Net unit price once &#x60;min_quantity&#x60; is reached. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PriceTier.new(
  customer_group_id: null,
  min_quantity: null,
  product_id: null,
  unit_price: null
)
```

