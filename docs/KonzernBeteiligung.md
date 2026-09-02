# SimplebillyApi::KonzernBeteiligung

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_name** | **String** |  |  |
| **control_basis** | **Array&lt;String&gt;** | Erfüllte Kontroll-Indikatoren (§ 290 Abs. 2 HGB) als deutsche Bezeichnungen. |  |
| **controlled** | **Boolean** |  |  |
| **ownership_pct** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::KonzernBeteiligung.new(
  company_name: null,
  control_basis: null,
  controlled: null,
  ownership_pct: null
)
```

