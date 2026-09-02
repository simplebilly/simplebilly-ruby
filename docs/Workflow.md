# SimplebillyApi::Workflow

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **actions** | **Object** |  | [optional] |
| **enabled** | **Boolean** |  | [optional] |
| **name** | **String** |  |  |
| **trigger_event** | **String** | Event that triggers the workflow, e.g. &#x60;order.paid&#x60;, &#x60;order.shipped&#x60;. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Workflow.new(
  actions: null,
  enabled: null,
  name: null,
  trigger_event: null
)
```

