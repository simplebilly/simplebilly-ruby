# SimplebillyApi::HebesatzLookup

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bundesland** | **String** |  |  |
| **country_code** | **String** |  |  |
| **gemeinde_name** | **String** |  |  |
| **gemeindeschluessel** | **String** |  |  |
| **hebesatz_gewerbesteuer** | **Float** |  |  |
| **hebesatz_grundsteuer_b** | **Float** |  | [optional] |
| **jahr** | **Integer** |  |  |
| **landkreis** | **String** |  | [optional] |
| **valid_from** | **String** |  |  |
| **valid_to** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::HebesatzLookup.new(
  bundesland: null,
  country_code: null,
  gemeinde_name: null,
  gemeindeschluessel: null,
  hebesatz_gewerbesteuer: null,
  hebesatz_grundsteuer_b: null,
  jahr: null,
  landkreis: null,
  valid_from: null,
  valid_to: null
)
```

