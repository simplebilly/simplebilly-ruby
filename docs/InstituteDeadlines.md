# SimplebillyApi::InstituteDeadlines

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **abschlusspruefung_months** | **Integer** | HGB § 340k/§ 341k: Abschlussprüfung (5 Monate). | [optional] |
| **jahresabschluss_bafin_months** | **Integer** | KWG § 26: Jahresabschluss an die BaFin (3 Monate, nur KWG-Institute). | [optional] |
| **offenlegung_months** | **Integer** | HGB § 325 Abs. 4: Offenlegung (4 kapitalmarktorientiert / 12 sonst). |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::InstituteDeadlines.new(
  abschlusspruefung_months: null,
  jahresabschluss_bafin_months: null,
  offenlegung_months: null
)
```

