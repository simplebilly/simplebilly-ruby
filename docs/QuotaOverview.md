# SimplebillyApi::QuotaOverview

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **features** | [**PlanFeatures**](PlanFeatures.md) |  |  |
| **is_trialing** | **Boolean** |  |  |
| **limits** | [**PlanLimits**](PlanLimits.md) |  |  |
| **metered** | [**Array&lt;MeteredUsage&gt;**](MeteredUsage.md) |  |  |
| **plan** | **String** |  |  |
| **plan_name** | **String** |  |  |
| **trial_ends_at** | **Time** |  | [optional] |
| **usage** | [**UsageSnapshot**](UsageSnapshot.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::QuotaOverview.new(
  features: null,
  is_trialing: null,
  limits: null,
  metered: null,
  plan: null,
  plan_name: null,
  trial_ends_at: null,
  usage: null
)
```

