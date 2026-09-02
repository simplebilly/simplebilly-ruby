# SimplebillyApi::PlausibilitySummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **errors** | **Integer** |  |  |
| **overall_status** | [**CheckStatus**](CheckStatus.md) |  |  |
| **passed** | **Integer** |  |  |
| **total_checks** | **Integer** |  |  |
| **warnings** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PlausibilitySummary.new(
  errors: null,
  overall_status: null,
  passed: null,
  total_checks: null,
  warnings: null
)
```

