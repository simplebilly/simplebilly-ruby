# SimplebillyApi::QuotaOverride

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **features** | [**QuotaOverrideFeatures**](QuotaOverrideFeatures.md) |  | [optional] |
| **max_connectors** | **Integer** |  | [optional] |
| **max_invoices_per_month** | **Integer** |  | [optional] |
| **max_users** | **Integer** |  | [optional] |
| **metered** | **Hash&lt;String, Integer&gt;** |  | [optional] |
| **plan** | **String** | Custom plan id; unknown ids resolve to enterprise limits. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::QuotaOverride.new(
  features: null,
  max_connectors: null,
  max_invoices_per_month: null,
  max_users: null,
  metered: null,
  plan: null
)
```

