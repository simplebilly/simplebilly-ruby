# SimplebillyApi::FeatureSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **onlineshop** | **Boolean** | Online shop / storefront module (default: enabled). |  |
| **report_bilanz** | **Boolean** | Bilanz (balance sheet) report. |  |
| **report_bwa** | **Boolean** | BWA (betriebswirtschaftliche Auswertung). |  |
| **report_euer** | **Boolean** | EÜR (Einnahmen-Überschuss-Rechnung). |  |
| **report_gewerbesteuer** | **Boolean** | Gewerbesteuer report. |  |
| **report_guv** | **Boolean** | GuV (profit &amp; loss) report. |  |
| **report_kst** | **Boolean** | KSt (Körperschaftsteuer) report. |  |
| **report_ustva** | **Boolean** | UStVA (Umsatzsteuervoranmeldung). |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::FeatureSettings.new(
  onlineshop: null,
  report_bilanz: null,
  report_bwa: null,
  report_euer: null,
  report_gewerbesteuer: null,
  report_guv: null,
  report_kst: null,
  report_ustva: null
)
```

