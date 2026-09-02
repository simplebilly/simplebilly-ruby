# SimplebillyApi::ComplianceTraining

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **assignable** | **Boolean** | Whether HR can assign this training as required for employees. | [optional] |
| **code** | **String** | Stable code used by plugins and frontend players (e.g. \&quot;data_privacy\&quot;). | [optional] |
| **created_at** | **Time** |  | [optional] |
| **deleted_at** | **Time** |  | [optional] |
| **description** | **String** |  | [optional] |
| **id** | **String** |  | [optional] |
| **pass_score** | **Integer** | Minimum score (0–100) required to pass. | [optional] |
| **plugin_platform** | **String** | Marketplace plugin platform id when source &#x3D; Plugin. | [optional] |
| **source** | [**TrainingSource**](TrainingSource.md) |  | [optional] |
| **tenant_id** | **String** |  | [optional] |
| **title** | **String** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |
| **validity_months** | **Integer** | Certificate validity in months; null &#x3D; no expiry. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ComplianceTraining.new(
  assignable: null,
  code: null,
  created_at: null,
  deleted_at: null,
  description: null,
  id: null,
  pass_score: null,
  plugin_platform: null,
  source: null,
  tenant_id: null,
  title: null,
  updated_at: null,
  validity_months: null
)
```

