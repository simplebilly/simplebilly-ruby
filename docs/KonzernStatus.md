# SimplebillyApi::KonzernStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **groessenbefreit** | **Boolean** |  |  |
| **kapitalmarktorientiert** | **Boolean** |  |  |
| **konzernabschlusspflicht** | **Boolean** |  |  |
| **missing_group_figures** | **Boolean** | Keine group_figures-Zeile für das Jahr vorhanden → keine Größenbefreiung. |  |
| **mutterunternehmen** | **Boolean** | Mutterunternehmen: mindestens eine beherrschte Beteiligung (§ 290 Abs. 1 HGB). |  |
| **parent_name** | **String** | Mutterunternehmen für die Zwischenholding-Befreiung (§ 291 HGB). | [optional] |
| **parent_situs** | **String** |  | [optional] |
| **participations** | [**Array&lt;KonzernBeteiligung&gt;**](KonzernBeteiligung.md) |  |  |
| **thresholds** | [**KonzernThresholds**](KonzernThresholds.md) |  |  |
| **year** | **Integer** |  |  |
| **zwischenholding_befreit** | **Boolean** |  |  |
| **zwischenholding_hinweis** | **String** | Hinweis zu den § 291-Voraussetzungen (EU/EWR-Sitz, geprüfter Konzernabschluss). | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::KonzernStatus.new(
  groessenbefreit: null,
  kapitalmarktorientiert: null,
  konzernabschlusspflicht: null,
  missing_group_figures: null,
  mutterunternehmen: null,
  parent_name: null,
  parent_situs: null,
  participations: null,
  thresholds: null,
  year: null,
  zwischenholding_befreit: null,
  zwischenholding_hinweis: null
)
```

