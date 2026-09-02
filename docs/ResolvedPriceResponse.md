# SimplebillyApi::ResolvedPriceResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **is_list_price** | **Boolean** | True when no tier matched and the product list price was used. |  |
| **price_tier_id** | **String** | Applied tier, if any matched. | [optional] |
| **product_id** | **String** |  |  |
| **quantity** | **Integer** |  |  |
| **unit_price** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ResolvedPriceResponse.new(
  is_list_price: null,
  price_tier_id: null,
  product_id: null,
  quantity: null,
  unit_price: null
)
```

