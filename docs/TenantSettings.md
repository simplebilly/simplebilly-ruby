# SimplebillyApi::TenantSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_type** | [**CompanyType**](CompanyType.md) |  |  |
| **dpa_accepted_at** | **Time** |  | [optional] |
| **dpa_accepted_by** | **String** |  | [optional] |
| **dpa_version** | **String** |  | [optional] |
| **features** | **Object** | Active feature toggles for the tenant. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TenantSettings.new(
  company_type: null,
  dpa_accepted_at: null,
  dpa_accepted_by: null,
  dpa_version: null,
  features: null
)
```

