# SimplebillyApi::RateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer** | [**CustomerInfo**](CustomerInfo.md) |  | [optional] |
| **packages** | [**Array&lt;Package&gt;**](Package.md) |  |  |
| **recipient** | [**Address**](Address.md) |  |  |
| **sender** | [**Address**](Address.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::RateRequest.new(
  customer: null,
  packages: null,
  recipient: null,
  sender: null
)
```

