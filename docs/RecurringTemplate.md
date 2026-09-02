# SimplebillyApi::RecurringTemplate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created_at** | **String** |  | [readonly] |
| **deleted_at** | **String** |  | [optional][readonly] |
| **end_date** | **Date** |  | [optional] |
| **execution_interval** | **String** |  |  |
| **execution_status** | **String** |  |  |
| **finalize** | **Boolean** |  |  |
| **last_executed_at** | **Time** |  | [optional] |
| **name** | **String** |  |  |
| **next_execution_at** | **Time** |  | [optional] |
| **start_date** | **Date** |  |  |
| **template_id** | **String** |  |  |
| **template_type** | **String** |  |  |
| **updated_at** | **String** |  | [optional][readonly] |
| **voucher_data** | **Object** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::RecurringTemplate.new(
  created_at: null,
  deleted_at: null,
  end_date: null,
  execution_interval: null,
  execution_status: null,
  finalize: null,
  last_executed_at: null,
  name: null,
  next_execution_at: null,
  start_date: null,
  template_id: null,
  template_type: null,
  updated_at: null,
  voucher_data: null
)
```

