# SimplebillyApi::ReturnLogisticsSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **by_status** | **Object** | Number of return orders per status. |  |
| **by_warehouse** | [**Array&lt;ReturnWarehouseSummary&gt;**](ReturnWarehouseSummary.md) | Per-warehouse aggregation. |  |
| **items_restocked** | **Integer** | Sum of &#x60;restock: true&#x60; line-item quantities. |  |
| **items_scrapped** | **Integer** | Sum of &#x60;restock: false&#x60; line-item quantities (scrapped/disposed). |  |
| **total_items** | **Integer** | Sum of all line-item quantities across returns. |  |
| **total_returns** | **Integer** | Total number of return orders (excluding soft-deleted). |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReturnLogisticsSummary.new(
  by_status: null,
  by_warehouse: null,
  items_restocked: null,
  items_scrapped: null,
  total_items: null,
  total_returns: null
)
```

