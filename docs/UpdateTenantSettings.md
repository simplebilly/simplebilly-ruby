# SimplebillyApi::UpdateTenantSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_type** | [**CompanyType**](CompanyType.md) |  |  |
| **features** | [**PartialFeatureSettings**](PartialFeatureSettings.md) |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::UpdateTenantSettings.new(
  company_type: null,
  features: null
)
```

