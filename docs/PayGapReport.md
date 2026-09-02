# SimplebillyApi::PayGapReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **by_job_title** | [**Array&lt;JobTitleGap&gt;**](JobTitleGap.md) |  |  |
| **diverse_count** | **Integer** |  |  |
| **employee_count** | **Integer** |  |  |
| **female_count** | **Integer** |  |  |
| **male_count** | **Integer** |  |  |
| **mean_gap_pct** | **Float** |  |  |
| **median_gap_pct** | **Float** |  |  |
| **quartiles** | [**Array&lt;QuartileBand&gt;**](QuartileBand.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayGapReport.new(
  by_job_title: null,
  diverse_count: null,
  employee_count: null,
  female_count: null,
  male_count: null,
  mean_gap_pct: null,
  median_gap_pct: null,
  quartiles: null
)
```

