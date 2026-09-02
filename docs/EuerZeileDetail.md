# SimplebillyApi::EuerZeileDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **abschnitt** | **String** |  |  |
| **betrag_gesamt** | **String** |  |  |
| **bezeichnung** | **String** |  |  |
| **kategorien** | [**Array&lt;EuerKatSumme&gt;**](EuerKatSumme.md) |  |  |
| **zeile** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EuerZeileDetail.new(
  abschnitt: null,
  betrag_gesamt: null,
  bezeichnung: null,
  kategorien: null,
  zeile: null
)
```

