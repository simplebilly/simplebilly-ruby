# SimplebillyApi::Coupon

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **discount_type** | [**DiscountType**](DiscountType.md) |  |  |
| **discount_value** | **String** |  |  |
| **expires_at** | **Time** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **is_combineable** | **Boolean** |  | [optional] |
| **max_discount_amount** | **String** |  | [optional] |
| **max_uses** | **Integer** |  | [optional] |
| **max_uses_per_customer** | **Integer** |  | [optional] |
| **min_order_amount** | **String** |  | [optional] |
| **product_ids** | **Object** |  | [optional] |
| **starts_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Coupon.new(
  code: null,
  description: null,
  discount_type: null,
  discount_value: null,
  expires_at: null,
  is_active: null,
  is_combineable: null,
  max_discount_amount: null,
  max_uses: null,
  max_uses_per_customer: null,
  min_order_amount: null,
  product_ids: null,
  starts_at: null
)
```

