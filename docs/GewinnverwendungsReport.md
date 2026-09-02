# SimplebillyApi::GewinnverwendungsReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bilanzgewinn** | **String** | Bilanzgewinn nach Einstellung (§ 174 AktG, Beschluss der HV). |  |
| **gesetzliche_ruecklage_bestand** | **String** |  |  |
| **gesetzliche_ruecklage_cap** | **String** | Deckel: 10 % des Grundkapitals (§ 150 Abs. 2 AktG). |  |
| **gesetzliche_ruecklage_nach** | **String** | Rücklage nach Einstellung. |  |
| **gesetzliche_ruecklage_soll** | **String** | Vorgeschlagene Einstellung in die gesetzliche Rücklage (§ 150 Abs. 2 AktG). |  |
| **gezeichnetes_kapital** | **String** |  |  |
| **jahresueberschuss** | **String** |  |  |
| **year** | **Integer** |  |  |
| **zeilen** | [**Array&lt;GewinnverwendungsZeile&gt;**](GewinnverwendungsZeile.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GewinnverwendungsReport.new(
  bilanzgewinn: null,
  gesetzliche_ruecklage_bestand: null,
  gesetzliche_ruecklage_cap: null,
  gesetzliche_ruecklage_nach: null,
  gesetzliche_ruecklage_soll: null,
  gezeichnetes_kapital: null,
  jahresueberschuss: null,
  year: null,
  zeilen: null
)
```

