# SimplebillyApi::PublicReturnRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** |  |  |
| **items** | [**Array&lt;PublicReturnItem&gt;**](PublicReturnItem.md) |  |  |
| **notes** | **String** |  | [optional] |
| **order_number** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PublicReturnRequest.new(
  email: null,
  items: null,
  notes: null,
  order_number: null
)
```

