# SimplebillyApi::ReorderProposalResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **generated_at** | **Time** |  |  |
| **lines** | [**Array&lt;ReorderProposalLine&gt;**](ReorderProposalLine.md) |  |  |
| **total_suggested_quantity** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ReorderProposalResponse.new(
  generated_at: null,
  lines: null,
  total_suggested_quantity: null
)
```

