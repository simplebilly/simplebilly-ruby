# SimplebillyApi::KontoReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **generated_at** | **String** |  |  |
| **konten** | [**Array&lt;KontoItem&gt;**](KontoItem.md) |  |  |
| **period** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::KontoReport.new(
  generated_at: null,
  konten: null,
  period: null
)
```

