# SimplebillyApi::Automation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **automation_key** | **String** |  |  |
| **config** | **Object** |  |  |
| **created_at** | **Time** |  |  |
| **enabled** | **Boolean** |  |  |
| **last_run_at** | **Time** |  | [optional] |
| **next_run_at** | **Time** |  | [optional] |
| **tenant_id** | **String** |  |  |
| **updated_at** | **Time** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Automation.new(
  automation_key: null,
  config: null,
  created_at: null,
  enabled: null,
  last_run_at: null,
  next_run_at: null,
  tenant_id: null,
  updated_at: null
)
```

