# SimplebillyApi::BilanzReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **aktiva** | [**Array&lt;BilanzItem&gt;**](BilanzItem.md) |  |  |
| **balanced** | **Boolean** |  |  |
| **generated_at** | **String** |  |  |
| **passiva** | [**Array&lt;BilanzItem&gt;**](BilanzItem.md) |  |  |
| **period** | **String** |  |  |
| **total_aktiva** | **String** |  |  |
| **total_passiva** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::BilanzReport.new(
  aktiva: null,
  balanced: null,
  generated_at: null,
  passiva: null,
  period: null,
  total_aktiva: null,
  total_passiva: null
)
```

