# SimplebillyApi::ReturnLogisticsQueueItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **age_days** | **Integer** | Days since creation, oldest first. |  |
| **created_at** | **Time** |  |  |
| **customer_name** | **String** |  | [optional] |
| **line_items** | **Object** |  |  |
| **order_number** | **String** |  | [optional] |
| **return_number** | **String** |  |  |
| **return_order_id** | **String** |  |  |
| **status** | **String** |  |  |
| **warehouse_id** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReturnLogisticsQueueItem.new(
  age_days: null,
  created_at: null,
  customer_name: null,
  line_items: null,
  order_number: null,
  return_number: null,
  return_order_id: null,
  status: null,
  warehouse_id: null
)
```

