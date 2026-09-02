# SimplebillyApi::TimeEntryDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **clock_in** | **Time** |  | [optional] |
| **clock_out** | **Time** |  | [optional] |
| **created_at** | **Time** |  |  |
| **date** | **Date** |  |  |
| **employee_id** | **String** |  |  |
| **hours** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **time_entry_id** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TimeEntryDto.new(
  clock_in: null,
  clock_out: null,
  created_at: null,
  date: null,
  employee_id: null,
  hours: null,
  notes: null,
  time_entry_id: null
)
```

