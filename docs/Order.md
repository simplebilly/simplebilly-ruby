# SimplebillyApi::Order

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **audit_log** | **Object** |  | [optional] |
| **currency** | **String** |  |  |
| **customer_id** | **String** | References the customer entity. |  |
| **external_reference** | **String** |  | [optional] |
| **invoice_address** | **Object** |  | [optional] |
| **items** | **Object** |  | [optional] |
| **language** | [**LanguageCode**](LanguageCode.md) |  | [optional] |
| **order_status** | [**OrderStatus**](OrderStatus.md) |  |  |
| **payment_method** | [**PaymentMethod**](PaymentMethod.md) |  |  |
| **shipping_address** | **Object** |  | [optional] |
| **shipping_cost** | **String** |  |  |
| **shipping_method** | **String** |  |  |
| **shipping_weight** | **String** |  |  |
| **tags** | **Array&lt;String&gt;** |  |  |
| **total_cost** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Order.new(
  audit_log: null,
  currency: null,
  customer_id: null,
  external_reference: null,
  invoice_address: null,
  items: null,
  language: null,
  order_status: null,
  payment_method: null,
  shipping_address: null,
  shipping_cost: null,
  shipping_method: null,
  shipping_weight: null,
  tags: null,
  total_cost: null
)
```

