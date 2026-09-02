# SimplebillyApi::AiWorkerConfig

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auto_reply** | **Boolean** |  |  |
| **created_at** | **Time** |  |  |
| **id** | **String** |  |  |
| **is_active** | **Boolean** |  |  |
| **max_tool_calls** | **Integer** |  |  |
| **model** | **String** |  |  |
| **name** | **String** |  |  |
| **provider** | **String** |  |  |
| **system_prompt** | **String** |  |  |
| **tenant_id** | **String** |  |  |
| **trigger_on** | **Array&lt;String&gt;** |  |  |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AiWorkerConfig.new(
  auto_reply: null,
  created_at: null,
  id: null,
  is_active: null,
  max_tool_calls: null,
  model: null,
  name: null,
  provider: null,
  system_prompt: null,
  tenant_id: null,
  trigger_on: null,
  updated_at: null
)
```

