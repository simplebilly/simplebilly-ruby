# SimplebillyApi::EmissionTarget

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **base_value** | **String** |  |  |
| **base_year** | **Integer** | tCO2e in the base year (actuals). |  |
| **description** | **String** | Transition-plan narrative (ESRS E1-1 light), may be empty. |  |
| **scope** | [**EmissionTargetScope**](EmissionTargetScope.md) | \&quot;total\&quot; | \&quot;1\&quot; | \&quot;2\&quot; | \&quot;3\&quot;. |  |
| **target_value** | **String** |  |  |
| **target_year** | **Integer** | tCO2e target for the target year. |  |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EmissionTarget.new(
  base_value: null,
  base_year: null,
  description: null,
  scope: null,
  target_value: null,
  target_year: null,
  updated_at: null
)
```

