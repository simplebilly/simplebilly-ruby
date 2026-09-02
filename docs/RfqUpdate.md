# SimplebillyApi::RfqUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | **String** |  | [optional] |
| **line_items** | **Object** | JSON array of &#x60;{product_id, name, sku, quantity, requested_unit_price?, quoted_unit_price?}&#x60;. | [optional] |
| **notes** | **String** |  | [optional] |
| **requested_date** | **Date** |  | [optional] |
| **response_date** | **Date** |  | [optional] |
| **rfq_number** | **String** |  | [optional] |
| **status** | [**RfqStatus**](RfqStatus.md) | One of: draft | sent | offer_received | rejected | converted | [optional] |
| **supplier_contact_id** | **String** | References the supplier entity. | [optional] |
| **supplier_name** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::RfqUpdate.new(
  currency: null,
  line_items: null,
  notes: null,
  requested_date: null,
  response_date: null,
  rfq_number: null,
  status: null,
  supplier_contact_id: null,
  supplier_name: null
)
```

