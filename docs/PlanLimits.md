# SimplebillyApi::PlanLimits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **max_connectors** | **Integer** |  |  |
| **max_invoices_per_month** | **Integer** |  |  |
| **max_users** | **Integer** |  |  |
| **metered** | **Hash&lt;String, Integer&gt;** |  | [optional] |
| **paid_connectors** | **Array&lt;String&gt;** | Connectors that are *not* included in this plan (require a higher tier). Empty &#x3D; all connectors included on this plan. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PlanLimits.new(
  max_connectors: null,
  max_invoices_per_month: null,
  max_users: null,
  metered: null,
  paid_connectors: null
)
```

