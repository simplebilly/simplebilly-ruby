# SimplebillyApi::EmissionsReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **by_category** | [**Array&lt;CategoryTotal&gt;**](CategoryTotal.md) |  |  |
| **by_scope** | [**Array&lt;ScopeTotal&gt;**](ScopeTotal.md) |  |  |
| **by_year** | [**Array&lt;YearTotal&gt;**](YearTotal.md) |  |  |
| **data_quality** | [**DataQuality**](DataQuality.md) |  |  |
| **intensity_per_employee** | **Float** |  | [optional] |
| **intensity_per_revenue_mio** | **Float** | tCO2e per million EUR net revenue. | [optional] |
| **net_revenue** | **Float** | Sum of paid/sent/partially-paid invoices (EUR net) in the year. | [optional] |
| **spend_based_estimate_tco2e** | **Float** | Spend-based estimate from bookkeeping payments (EXIOBASE factor). | [optional] |
| **targets** | [**Array&lt;TargetProgress&gt;**](TargetProgress.md) |  |  |
| **total_tco2e** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EmissionsReport.new(
  by_category: null,
  by_scope: null,
  by_year: null,
  data_quality: null,
  intensity_per_employee: null,
  intensity_per_revenue_mio: null,
  net_revenue: null,
  spend_based_estimate_tco2e: null,
  targets: null,
  total_tco2e: null
)
```

