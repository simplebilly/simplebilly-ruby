# SimplebillyApi::PlausibilityReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **checks** | [**Array&lt;PlausibilityCheck&gt;**](PlausibilityCheck.md) |  |  |
| **generated_at** | **String** |  |  |
| **summary** | [**PlausibilitySummary**](PlausibilitySummary.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PlausibilityReport.new(
  checks: null,
  generated_at: null,
  summary: null
)
```

