# SimplebillyApi::PayrollCreatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **employee_ids** | **Array&lt;String&gt;** |  |  |
| **extra_payments** | [**Array&lt;ExtraPayment&gt;**](ExtraPayment.md) |  | [optional] |
| **month** | **Integer** |  |  |
| **year** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PayrollCreatePayload.new(
  employee_ids: null,
  extra_payments: null,
  month: null,
  year: null
)
```

