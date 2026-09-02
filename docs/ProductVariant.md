# SimplebillyApi::ProductVariant

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **barcode** | **String** |  | [optional] |
| **image_link** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **name** | **String** | Human-readable variant label, e.g. \&quot;Red / M\&quot;. | [optional] |
| **option_values** | **Object** | Option name → value map, e.g. &#x60;{\&quot;Color\&quot;: \&quot;Red\&quot;, \&quot;Size\&quot;: \&quot;M\&quot;}&#x60;. | [optional] |
| **price** | **String** | Explicit override price for this variant (takes precedence over parent price + delta). | [optional] |
| **price_delta** | **String** | Price adjustment relative to the parent product&#39;s &#x60;default_price&#x60;. | [optional] |
| **product_id** | **String** | The parent product this variant belongs to. References the product entity. |  |
| **sku** | **String** | Variant-specific SKU (must be unique per tenant). |  |
| **stock_quantity** | **Integer** | Variant-level stock (optional — may be tracked on the parent only). | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProductVariant.new(
  barcode: null,
  image_link: null,
  is_active: null,
  name: null,
  option_values: null,
  price: null,
  price_delta: null,
  product_id: null,
  sku: null,
  stock_quantity: null
)
```

