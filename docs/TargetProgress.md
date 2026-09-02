# SimplebillyApi::TargetProgress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **base_value** | **Float** |  |  |
| **base_year** | **Integer** |  |  |
| **description** | **String** |  |  |
| **id** | **String** |  |  |
| **progress_pct** | **Float** | Current year&#39;s emissions for the scope as % of the target. None when no data. | [optional] |
| **scope** | **String** |  |  |
| **target_value** | **Float** |  |  |
| **target_year** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TargetProgress.new(
  base_value: null,
  base_year: null,
  description: null,
  id: null,
  progress_pct: null,
  scope: null,
  target_value: null,
  target_year: null
)
```

