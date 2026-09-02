# SimplebillyApi::ProductCategoryUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **parent_category_id** | **String** | References the category entity. | [optional] |
| **sort_order** | **Integer** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProductCategoryUpdate.new(
  description: null,
  name: null,
  parent_category_id: null,
  sort_order: null
)
```

