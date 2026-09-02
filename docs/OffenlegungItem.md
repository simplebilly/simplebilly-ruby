# SimplebillyApi::OffenlegungItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **exists** | **Boolean** | Ob die zugrunde liegenden Daten im System vorhanden sind. |  |
| **name** | **String** | Bezeichnung des Offenlegungsbestandteils (§ 325 Abs. 1 HGB). |  |
| **source** | **String** | Woher der Bestandteil stammt bzw. fehlt. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::OffenlegungItem.new(
  exists: null,
  name: null,
  source: null
)
```

