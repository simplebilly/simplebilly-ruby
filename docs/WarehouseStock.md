# SimplebillyApi::WarehouseStock

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_number** | **String** | Batch/lot number (Chargennummer) — &#x60;None&#x60; for non-batched goods. | [optional] |
| **bin_location** | **String** |  | [optional] |
| **expiry_date** | **Date** | Expiry date for batch-tracked goods. | [optional] |
| **product_id** | **String** |  |  |
| **quantity** | **Integer** |  |  |
| **serial_numbers** | **Object** | JSON array of serial numbers (Seriennummern) in this stock row. | [optional] |
| **warehouse_id** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::WarehouseStock.new(
  batch_number: null,
  bin_location: null,
  expiry_date: null,
  product_id: null,
  quantity: null,
  serial_numbers: null,
  warehouse_id: null
)
```

