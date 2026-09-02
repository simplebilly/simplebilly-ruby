# SimplebillyApi::ComplianceTrainingUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **assignable** | **Boolean** | Whether HR can assign this training as required for employees. | [optional] |
| **code** | **String** | Stable code used by plugins and frontend players (e.g. \&quot;data_privacy\&quot;). | [optional] |
| **description** | **String** |  | [optional] |
| **pass_score** | **Integer** | Minimum score (0–100) required to pass. | [optional] |
| **plugin_platform** | **String** | Marketplace plugin platform id when source &#x3D; Plugin. | [optional] |
| **source** | [**TrainingSource**](TrainingSource.md) |  | [optional] |
| **title** | **String** |  | [optional] |
| **validity_months** | **Integer** | Certificate validity in months; null &#x3D; no expiry. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ComplianceTrainingUpdate.new(
  assignable: null,
  code: null,
  description: null,
  pass_score: null,
  plugin_platform: null,
  source: null,
  title: null,
  validity_months: null
)
```

