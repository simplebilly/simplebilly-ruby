# SimplebillyApi::SilentPartnerCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contract_date** | **Date** | Datum des Vertragsabschlusses. | [optional] |
| **einlage** | **String** | Einlage (§ 230 HGB). | [optional] |
| **gewinnquote_pct** | **String** | Gewinnbeteiligungsquote in Prozent (§ 231 HGB). | [optional] |
| **gewinnvortrag** | **String** | Nicht erhobene Gewinne (§ 232 Abs. 3 HGB). | [optional] |
| **instrument_type** | [**InstrumentType**](InstrumentType.md) | Instrument: \&quot;typisch\&quot; | \&quot;atypisch\&quot; | \&quot;partiarisches_darlehen\&quot; | \&quot;genussrecht\&quot;. |  |
| **kest_pflichtig** | **Boolean** | 25 % Kapitalertragsteuer einbehalten (§ 43 Abs. 1 Nr. 3 EStG; typisch + partiarisches Darlehen). | [optional] |
| **name** | **String** | Name des stillen Gesellschafters. | [optional] |
| **notes** | **String** | Freitext-Notizen. | [optional] |
| **verlust_verrechnungskonto** | **String** | Kumulierte Verluste gegen die Einlage (§ 232 Abs. 2 HGB, ≤ Einlage). | [optional] |
| **verlustbeteiligung** | **Boolean** | Verlustbeteiligung (§ 231 Abs. 2 HGB; kann ausgeschlossen werden). | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SilentPartnerCreate.new(
  contract_date: null,
  einlage: null,
  gewinnquote_pct: null,
  gewinnvortrag: null,
  instrument_type: null,
  kest_pflichtig: null,
  name: null,
  notes: null,
  verlust_verrechnungskonto: null,
  verlustbeteiligung: null
)
```

