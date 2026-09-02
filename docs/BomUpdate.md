# SimplebillyApi::BomUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **components** | **Object** | JSON array of &#x60;{product_id, name, quantity, unit, scrap_rate}&#x60;. | [optional] |
| **description** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **output_quantity** | **Integer** | Output quantity per production run (defaults to 1). | [optional] |
| **product_id** | **String** | The finished product this BOM produces. References the product entity. | [optional] |
| **status** | [**BomStatus**](BomStatus.md) | One of: draft | active | archived | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BomUpdate.new(
  components: null,
  description: null,
  name: null,
  output_quantity: null,
  product_id: null,
  status: null
)
```

