# SimplebillyApi::OrderUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **audit_log** | **Object** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **customer_id** | **String** | References the customer entity. | [optional] |
| **external_reference** | **String** |  | [optional] |
| **invoice_address** | **Object** |  | [optional] |
| **items** | **Object** |  | [optional] |
| **language** | [**LanguageCode**](LanguageCode.md) |  | [optional] |
| **order_status** | [**OrderStatus**](OrderStatus.md) |  | [optional] |
| **payment_method** | [**PaymentMethod**](PaymentMethod.md) |  | [optional] |
| **shipping_address** | **Object** |  | [optional] |
| **shipping_cost** | **String** |  | [optional] |
| **shipping_method** | **String** |  | [optional] |
| **shipping_weight** | **String** |  | [optional] |
| **tags** | **Array&lt;String&gt;** |  | [optional] |
| **total_cost** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::OrderUpdate.new(
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

