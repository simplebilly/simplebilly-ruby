# SimplebillyApi::GezReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **beitragsfreie_kfz** | **Integer** |  |  |
| **beitragspflichtige_kfz** | **Integer** |  |  |
| **betriebsstaetten** | [**Array&lt;BetriebsstaettenDetail&gt;**](BetriebsstaettenDetail.md) |  |  |
| **hinweis** | **String** |  |  |
| **hotelzimmer_beitrag** | **String** |  |  |
| **jaehrlicher_beitrag** | **String** |  |  |
| **jahr** | **Integer** |  |  |
| **kfz_beitrag** | **String** |  |  |
| **monatlicher_beitrag** | **String** |  |  |
| **vierteljaehrlicher_beitrag** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GezReport.new(
  beitragsfreie_kfz: null,
  beitragspflichtige_kfz: null,
  betriebsstaetten: null,
  hinweis: null,
  hotelzimmer_beitrag: null,
  jaehrlicher_beitrag: null,
  jahr: null,
  kfz_beitrag: null,
  monatlicher_beitrag: null,
  vierteljaehrlicher_beitrag: null
)
```

