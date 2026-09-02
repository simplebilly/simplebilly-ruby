# SimplebillyApi::EksErgebnis

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gesamtergebnis** | **String** |  |  |
| **monate** | [**Array&lt;EksMonatsWert&gt;**](EksMonatsWert.md) |  |  |
| **prognose_naechste_6_monate** | **String** |  |  |
| **summe_ausgaben** | **String** |  |  |
| **summe_einnahmen** | **String** |  |  |
| **zeitraum_bis** | **String** |  |  |
| **zeitraum_von** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EksErgebnis.new(
  gesamtergebnis: null,
  monate: null,
  prognose_naechste_6_monate: null,
  summe_ausgaben: null,
  summe_einnahmen: null,
  zeitraum_bis: null,
  zeitraum_von: null
)
```

