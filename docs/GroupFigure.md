# SimplebillyApi::GroupFigure

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bilanzsumme** | **String** | Bilanzsumme in EUR (§ 293 Abs. 1 Nr. 1 HGB). | [optional] |
| **exemption_claimed** | **Boolean** | § 291-Befreiung in Anspruch genommen. | [optional] |
| **mitarbeiter** | **Integer** | Durchschnittliche Arbeitnehmerzahl (§ 293 Abs. 1 Nr. 3 HGB). | [optional] |
| **netto_umsatz** | **String** | Netto-Umsatzerlöse in EUR (§ 293 Abs. 1 Nr. 2 HGB). | [optional] |
| **parent_name** | **String** | Name des Mutterunternehmens (§ 291 HGB, Zwischenholding). | [optional] |
| **parent_situs** | **String** | Sitz des Mutterunternehmens, z. B. \&quot;EU/EWR\&quot; (§ 291 HGB). | [optional] |
| **year** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GroupFigure.new(
  bilanzsumme: null,
  exemption_claimed: null,
  mitarbeiter: null,
  netto_umsatz: null,
  parent_name: null,
  parent_situs: null,
  year: null
)
```

