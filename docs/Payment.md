# SimplebillyApi::Payment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **String** |  | [optional] |
| **attachment** | **Object** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **customer_id** | **String** | References the customer entity. | [optional] |
| **description** | **String** |  | [optional] |
| **metadata** | **Object** |  | [optional] |
| **method** | [**PaymentMethod**](PaymentMethod.md) |  | [optional] |
| **payment_date** | **Time** |  | [optional] |
| **reference** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Payment.new(
  amount: null,
  attachment: null,
  currency: null,
  customer_id: null,
  description: null,
  metadata: null,
  method: null,
  payment_date: null,
  reference: null
)
```

