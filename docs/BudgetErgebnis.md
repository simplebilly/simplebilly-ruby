# SimplebillyApi::BudgetErgebnis

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **jahr** | **Integer** |  |  |
| **monat** | **Integer** |  |  |
| **monats_budget** | [**Array&lt;BudgetKategorie&gt;**](BudgetKategorie.md) |  |  |
| **prognose_restjahr** | [**Array&lt;BudgetKategorie&gt;**](BudgetKategorie.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BudgetErgebnis.new(
  jahr: null,
  monat: null,
  monats_budget: null,
  prognose_restjahr: null
)
```

