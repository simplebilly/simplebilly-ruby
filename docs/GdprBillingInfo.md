# SimplebillyApi::GdprBillingInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_period_end** | **Time** |  | [optional] |
| **current_period_start** | **Time** |  | [optional] |
| **plan** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **tenant_id** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GdprBillingInfo.new(
  current_period_end: null,
  current_period_start: null,
  plan: null,
  status: null,
  tenant_id: null
)
```

