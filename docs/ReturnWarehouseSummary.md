# SimplebillyApi::ReturnWarehouseSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items_restocked** | **Integer** |  |  |
| **items_scrapped** | **Integer** |  |  |
| **returns** | **Integer** |  |  |
| **warehouse_id** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReturnWarehouseSummary.new(
  items_restocked: null,
  items_scrapped: null,
  returns: null,
  warehouse_id: null
)
```

