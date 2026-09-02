# SimplebillyApi::Shipment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivered_at** | **Time** |  | [optional] |
| **label_url** | **String** |  | [optional] |
| **line_items_shipment** | **Object** |  | [optional] |
| **order_id** | **String** | References the order entity. |  |
| **recipient_address** | **Object** |  | [optional] |
| **shipment_date** | **Date** |  |  |
| **shipping_carrier** | **String** |  |  |
| **shipping_cost** | **String** |  | [optional] |
| **shipping_method** | **String** |  | [optional] |
| **signed_by** | **String** |  | [optional] |
| **status** | **String** |  |  |
| **tracking_events** | **Object** | Latest carrier tracking events (from the live tracking API). | [optional] |
| **tracking_number** | **String** |  | [optional] |
| **tracking_url** | **String** |  | [optional] |
| **weight_kg** | **Float** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Shipment.new(
  delivered_at: null,
  label_url: null,
  line_items_shipment: null,
  order_id: null,
  recipient_address: null,
  shipment_date: null,
  shipping_carrier: null,
  shipping_cost: null,
  shipping_method: null,
  signed_by: null,
  status: null,
  tracking_events: null,
  tracking_number: null,
  tracking_url: null,
  weight_kg: null
)
```

