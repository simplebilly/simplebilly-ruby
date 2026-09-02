# SimplebillyApi::EuerErgebnis

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **anlage_zugaenge** | **String** |  |  |
| **gewinn_verlust** | **String** |  |  |
| **jahr** | **Integer** |  |  |
| **summe_ausgaben** | **String** |  |  |
| **summe_einnahmen** | **String** |  |  |
| **zeilen** | [**Array&lt;EuerZeile&gt;**](EuerZeile.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EuerErgebnis.new(
  anlage_zugaenge: null,
  gewinn_verlust: null,
  jahr: null,
  summe_ausgaben: null,
  summe_einnahmen: null,
  zeilen: null
)
```

