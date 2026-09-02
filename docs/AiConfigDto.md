# SimplebillyApi::AiConfigDto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auto_reply** | **Boolean** |  | [optional] |
| **max_tool_calls** | **Integer** |  | [optional] |
| **model** | **String** |  |  |
| **name** | **String** |  |  |
| **provider** | **String** |  |  |
| **system_prompt** | **String** |  | [optional] |
| **trigger_on** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AiConfigDto.new(
  auto_reply: null,
  max_tool_calls: null,
  model: null,
  name: null,
  provider: null,
  system_prompt: null,
  trigger_on: null
)
```

