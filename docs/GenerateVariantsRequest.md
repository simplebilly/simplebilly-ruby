# SimplebillyApi::GenerateVariantsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **options** | **Hash&lt;String, Array&lt;String&gt;&gt;** | Option name → list of values, e.g. &#x60;{\&quot;Color\&quot;: [\&quot;Red\&quot;, \&quot;Blue\&quot;], \&quot;Size\&quot;: [\&quot;S\&quot;, \&quot;M\&quot;]}&#x60;. The cartesian product of these lists is generated. | [optional] |
| **price_delta** | **String** | Optional per-variant price delta applied to every generated variant. | [optional] |
| **product_id** | **String** |  |  |
| **sku_prefix** | **String** | Optional prefix for the generated SKUs (suffix is the option values joined by &#x60;-&#x60;). Falls back to the parent product&#39;s SKU. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GenerateVariantsRequest.new(
  options: null,
  price_delta: null,
  product_id: null,
  sku_prefix: null
)
```

