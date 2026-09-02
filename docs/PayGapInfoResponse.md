# SimplebillyApi::PayGapInfoResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **employee_id** | **String** |  |  |
| **first_name** | **String** |  |  |
| **gender** | **String** |  | [optional] |
| **group_median_hourly** | **Float** |  | [optional] |
| **group_median_monthly** | **Float** |  | [optional] |
| **group_size** | **Integer** |  |  |
| **job_title** | **String** |  |  |
| **last_name** | **String** |  |  |
| **overall_median_hourly** | **Float** |  | [optional] |
| **own_hourly_gross** | **Float** |  | [optional] |
| **own_monthly_gross** | **Float** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayGapInfoResponse.new(
  employee_id: null,
  first_name: null,
  gender: null,
  group_median_hourly: null,
  group_median_monthly: null,
  group_size: null,
  job_title: null,
  last_name: null,
  overall_median_hourly: null,
  own_hourly_gross: null,
  own_monthly_gross: null
)
```

