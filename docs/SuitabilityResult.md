# SimplebillyApi::SuitabilityResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **methods** | [**Array&lt;MethodSuitability&gt;**](MethodSuitability.md) |  |  |
| **recommended_box** | [**BoxFit**](BoxFit.md) |  | [optional] |
| **requires_insurance** | **Boolean** |  |  |
| **total_value** | **String** |  |  |
| **total_weight_kg** | **Float** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SuitabilityResult.new(
  methods: null,
  recommended_box: null,
  requires_insurance: null,
  total_value: null,
  total_weight_kg: null
)
```

