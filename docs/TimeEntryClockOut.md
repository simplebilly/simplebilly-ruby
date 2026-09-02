# SimplebillyApi::TimeEntryClockOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **clock_out** | **Time** |  |  |
| **hours** | **String** | Optional manual hours; when absent, derived from clock_in..clock_out. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TimeEntryClockOut.new(
  clock_out: null,
  hours: null
)
```

