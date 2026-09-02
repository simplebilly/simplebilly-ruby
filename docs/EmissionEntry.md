# SimplebillyApi::EmissionEntry

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_value** | **String** | Activity amount in &#x60;unit&#x60; (kWh, l, km, t, tkm, EUR). |  |
| **category_id** | **String** | GHG-Protocol category key, e.g. \&quot;purchased_goods\&quot;, \&quot;business_travel\&quot;. |  |
| **description** | **String** |  |  |
| **ef_source** | **String** | Emission-factor source, e.g. \&quot;UBA-2024\&quot;, \&quot;DEFRA-2024\&quot;. |  |
| **ef_version** | **String** |  |  |
| **method** | [**EmissionMethod**](EmissionMethod.md) | \&quot;activity\&quot; | \&quot;spend\&quot; | \&quot;supplier\&quot;. |  |
| **scope** | [**GhgScope**](GhgScope.md) | GHG scope: \&quot;1\&quot; | \&quot;2\&quot; | \&quot;3\&quot;. |  |
| **tco2e** | **String** | Computed server-side: activity * factor / 1000, rounded to 4 dp. |  |
| **unit** | **String** | Unit of the activity value. |  |
| **updated_at** | **Time** |  | [optional] |
| **year** | **Integer** | Reporting year. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EmissionEntry.new(
  activity_value: null,
  category_id: null,
  description: null,
  ef_source: null,
  ef_version: null,
  method: null,
  scope: null,
  tco2e: null,
  unit: null,
  updated_at: null,
  year: null
)
```

