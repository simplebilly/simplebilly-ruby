# SimplebillyApi::PackingQueueItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created_at** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **delivery_note_printed** | **Boolean** |  |  |
| **items** | **Object** |  |  |
| **items_count** | **Integer** |  |  |
| **label_printed** | **Boolean** |  |  |
| **order_number** | **String** |  |  |
| **order_status** | **String** |  |  |
| **shipment_id** | **String** |  | [optional] |
| **shipping_address** | **Object** |  | [optional] |
| **shipping_method** | **String** |  |  |
| **tracking_number** | **String** |  | [optional] |
| **video_recording** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PackingQueueItem.new(
  created_at: null,
  customer_id: null,
  delivery_note_printed: null,
  items: null,
  items_count: null,
  label_printed: null,
  order_number: null,
  order_status: null,
  shipment_id: null,
  shipping_address: null,
  shipping_method: null,
  tracking_number: null,
  video_recording: null
)
```

