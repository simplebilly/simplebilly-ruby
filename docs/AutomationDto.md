# SimplebillyApi::AutomationDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **automation_key** | **String** |  |  |
| **config** | **Object** |  |  |
| **default_day** | **Integer** |  | [optional] |
| **description** | **String** |  |  |
| **enabled** | **Boolean** |  |  |
| **kind** | **String** |  |  |
| **last_run_at** | **Time** |  | [optional] |
| **next_run_at** | **Time** |  | [optional] |
| **schedule_kind** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AutomationDto.new(
  automation_key: null,
  config: null,
  default_day: null,
  description: null,
  enabled: null,
  kind: null,
  last_run_at: null,
  next_run_at: null,
  schedule_kind: null
)
```

