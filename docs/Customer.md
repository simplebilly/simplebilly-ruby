# SimplebillyApi::Customer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **Object** |  | [optional] |
| **contact_person** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **external_order_number** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **payment_grace_period_days** | **Integer** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **vat_id** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Customer.new(
  address: null,
  contact_person: null,
  email: null,
  external_order_number: null,
  name: null,
  payment_grace_period_days: null,
  phone: null,
  vat_id: null
)
```

