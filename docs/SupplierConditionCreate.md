# SimplebillyApi::SupplierConditionCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | **String** | Currency for the minimum order value. |  |
| **delivery_terms** | **String** | Incoterms, e.g. \&quot;EXW\&quot;, \&quot;DAP\&quot;. | [optional] |
| **early_payment_discount_percent** | **String** | Early-payment discount percentage (Skonto), e.g. 2.0. | [optional] |
| **is_default** | **Boolean** | Is this the default condition for the supplier? | [optional] |
| **minimum_order_value** | **String** | Minimum order value required for this supplier. | [optional] |
| **notes** | **String** |  | [optional] |
| **payment_due_days** | **Integer** | Number of days within which payment is due. | [optional] |
| **payment_terms** | **String** | Payment terms, e.g. \&quot;14 Tage, 2% Skonto\&quot;. | [optional] |
| **supplier_contact_id** | **String** | The supplier this condition applies to (&#x60;contact_id&#x60;). References the supplier entity. |  |
| **supplier_name** | **String** | The name of the supplier, denormalized for easy listing. | [optional] |
| **volume_discount_tiers** | **Object** | Tiered discounts: JSON array of &#x60;{min_quantity, discount_percent}&#x60;. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SupplierConditionCreate.new(
  currency: null,
  delivery_terms: null,
  early_payment_discount_percent: null,
  is_default: null,
  minimum_order_value: null,
  notes: null,
  payment_due_days: null,
  payment_terms: null,
  supplier_contact_id: null,
  supplier_name: null,
  volume_discount_tiers: null
)
```

