# SimplebillyApi::ShippingRuleCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **carrier** | **String** | Provider that auto-filled this rule (e.g. \&quot;ups\&quot;), if any. | [optional] |
| **country** | [**CountryCode**](CountryCode.md) | None &#x3D; applies to all countries. | [optional] |
| **delivery_time** | **String** | Delivery time text, e.g. \&quot;1-3\&quot;. | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **max_weight_kg** | **Float** |  | [optional] |
| **min_weight_kg** | **Float** |  | [optional] |
| **name** | **String** | Delivery-method label, e.g. \&quot;Standardversand\&quot;. |  |
| **notes** | **String** |  | [optional] |
| **price** | **String** | Shipping cost in the shop&#39;s currency. |  |
| **priority** | **Integer** | Lower wins when multiple rules match. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ShippingRuleCreate.new(
  carrier: null,
  country: null,
  delivery_time: null,
  is_active: null,
  max_weight_kg: null,
  min_weight_kg: null,
  name: null,
  notes: null,
  price: null,
  priority: null
)
```

