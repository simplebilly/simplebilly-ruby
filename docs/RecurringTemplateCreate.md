# SimplebillyApi::RecurringTemplateCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **end_date** | **Date** |  | [optional] |
| **execution_interval** | **String** |  |  |
| **execution_status** | [**ExecutionStatus**](ExecutionStatus.md) |  |  |
| **finalize** | **Boolean** |  | [optional] |
| **last_executed_at** | **Time** |  | [optional] |
| **name** | **String** |  |  |
| **next_execution_at** | **Time** |  | [optional] |
| **start_date** | **Date** |  |  |
| **template_type** | [**RecurringTemplateType**](RecurringTemplateType.md) |  |  |
| **voucher_data** | **Object** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::RecurringTemplateCreate.new(
  end_date: null,
  execution_interval: null,
  execution_status: null,
  finalize: null,
  last_executed_at: null,
  name: null,
  next_execution_at: null,
  start_date: null,
  template_type: null,
  voucher_data: null
)
```

