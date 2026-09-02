# SimplebillyApi::InstituteStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **checklist** | [**Array&lt;InstituteCheckItem&gt;**](InstituteCheckItem.md) |  |  |
| **deadlines** | [**InstituteDeadlines**](InstituteDeadlines.md) |  |  |
| **institute_type** | **String** |  |  |
| **kapitalmarktorientiert** | **Boolean** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::InstituteStatus.new(
  checklist: null,
  deadlines: null,
  institute_type: null,
  kapitalmarktorientiert: null
)
```

