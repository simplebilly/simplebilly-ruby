# SimplebillyApi::OpenItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount_due** | **String** |  |  |
| **amount_paid** | **String** |  |  |
| **customer_id** | **String** |  | [optional] |
| **days_overdue** | **Integer** |  | [optional] |
| **due_date** | **String** |  | [optional] |
| **invoice_id** | **String** |  |  |
| **invoice_number** | **String** |  |  |
| **issue_date** | **String** |  |  |
| **open_amount** | **String** |  |  |
| **reminder_level** | [**ReminderLevel**](ReminderLevel.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::OpenItem.new(
  amount_due: null,
  amount_paid: null,
  customer_id: null,
  days_overdue: null,
  due_date: null,
  invoice_id: null,
  invoice_number: null,
  issue_date: null,
  open_amount: null,
  reminder_level: null
)
```

