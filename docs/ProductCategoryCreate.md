# SimplebillyApi::ProductCategoryCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **parent_category_id** | **String** | References the category entity. | [optional] |
| **sort_order** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProductCategoryCreate.new(
  description: null,
  name: null,
  parent_category_id: null,
  sort_order: null
)
```

