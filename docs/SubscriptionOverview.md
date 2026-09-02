# SimplebillyApi::SubscriptionOverview

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_period_end** | **Time** |  | [optional] |
| **features** | [**PlanFeatures**](PlanFeatures.md) |  |  |
| **is_trialing** | **Boolean** |  |  |
| **limits** | [**PlanLimits**](PlanLimits.md) |  |  |
| **manage_url** | **String** |  | [optional] |
| **plan** | **String** | Resolved plan id (free/starter/business/enterprise, or a custom override id). |  |
| **plan_name** | **String** |  |  |
| **price_eur** | **Float** | Monthly price in EUR; &#x60;-1.0&#x60; &#x3D; custom pricing (enterprise). |  |
| **quantity** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **subscription_id** | **String** |  | [optional] |
| **trial_ends_at** | **Time** |  | [optional] |
| **usage** | [**UsageSnapshot**](UsageSnapshot.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SubscriptionOverview.new(
  current_period_end: null,
  features: null,
  is_trialing: null,
  limits: null,
  manage_url: null,
  plan: null,
  plan_name: null,
  price_eur: null,
  quantity: null,
  status: null,
  subscription_id: null,
  trial_ends_at: null,
  usage: null
)
```

