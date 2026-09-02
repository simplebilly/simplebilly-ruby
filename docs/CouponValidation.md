# SimplebillyApi::CouponValidation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |
| **discount_type** | **String** |  |  |
| **discount_value** | **String** |  |  |
| **discounted_amount** | **String** |  |  |
| **max_discount_amount** | **String** |  | [optional] |
| **reason** | **String** |  | [optional] |
| **valid** | **Boolean** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CouponValidation.new(
  code: null,
  discount_type: null,
  discount_value: null,
  discounted_amount: null,
  max_discount_amount: null,
  reason: null,
  valid: null
)
```

