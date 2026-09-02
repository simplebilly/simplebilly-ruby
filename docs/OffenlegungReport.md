# SimplebillyApi::OffenlegungReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **deadline** | **Date** | Fristende (Abschlussstichtag + Frist). |  |
| **deadline_months** | **Integer** | Offenlegungsfrist in Monaten (§ 325 Abs. 4 HGB). |  |
| **items** | [**Array&lt;OffenlegungItem&gt;**](OffenlegungItem.md) |  |  |
| **kapitalmarktorientiert** | **Boolean** | Annahme über die Kapitalmarktorientierung. |  |
| **note** | **String** |  |  |
| **year** | **Integer** | Berichtsjahr (laufendes Kalenderjahr). |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::OffenlegungReport.new(
  deadline: null,
  deadline_months: null,
  items: null,
  kapitalmarktorientiert: null,
  note: null,
  year: null
)
```

