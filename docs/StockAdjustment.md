# SimplebillyApi::StockAdjustment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_number** | **String** |  | [optional] |
| **bin_location** | **String** |  | [optional] |
| **expiry_date** | **Date** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **quantity** | **Integer** |  |  |
| **serial_numbers** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::StockAdjustment.new(
  batch_number: null,
  bin_location: null,
  expiry_date: null,
  product_id: null,
  quantity: null,
  serial_numbers: null
)
```

