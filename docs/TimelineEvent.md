# SimplebillyApi::TimelineEvent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** | RFC3339 UTC timestamp for sorting. |  |
| **detail** | **String** |  | [optional] |
| **id** | **String** | Source record id (stringified). |  |
| **status** | **String** |  | [optional] |
| **title** | **String** |  |  |
| **type** | **String** | Source module: communication | quotation | order | invoice | attachment. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TimelineEvent.new(
  date: null,
  detail: null,
  id: null,
  status: null,
  title: null,
  type: null
)
```

