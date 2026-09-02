# SimplebillyApi::ProductAttribute

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **is_filterable** | **Boolean** | Whether this attribute participates in the shop&#39;s faceted filters. | [optional] |
| **name** | **String** | Attribute name, e.g. &#x60;Material&#x60;, &#x60;Farbe&#x60;, &#x60;Gewicht&#x60;. |  |
| **position** | **Integer** | Ordering position within the product&#39;s attribute list. | [optional] |
| **product_id** | **String** | The product this attribute belongs to. References the product entity. |  |
| **unit** | **String** | Optional unit of measure for numeric attributes, e.g. &#x60;g&#x60;, &#x60;cm&#x60;. | [optional] |
| **value** | **String** | Attribute value, e.g. &#x60;Baumwolle&#x60;, &#x60;Rot&#x60;, &#x60;180g&#x60;. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProductAttribute.new(
  is_filterable: null,
  name: null,
  position: null,
  product_id: null,
  unit: null,
  value: null
)
```

