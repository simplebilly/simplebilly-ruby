# SimplebillyApi::DeliveryDate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | References the customer entity. | [optional] |
| **fulfilled_date** | **Date** | Date actually delivered (set on fulfillment). | [optional] |
| **note** | **String** |  | [optional] |
| **order_number** | **String** | Sales order number (&#x60;order.order_number&#x60;). |  |
| **original_date** | **Date** | Original date promised before rescheduling. | [optional] |
| **product_id** | **String** | Product line item this date applies to, if per-item. References the product entity. | [optional] |
| **promised_date** | **Date** | Date promised to the customer. |  |
| **status** | [**DeliveryDateStatus**](DeliveryDateStatus.md) | One of: promised | confirmed | rescheduled | fulfilled | late | cancelled |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DeliveryDate.new(
  customer_id: null,
  fulfilled_date: null,
  note: null,
  order_number: null,
  original_date: null,
  product_id: null,
  promised_date: null,
  status: null
)
```

