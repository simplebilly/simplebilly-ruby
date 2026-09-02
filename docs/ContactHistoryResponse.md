# SimplebillyApi::ContactHistoryResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |
| **inbound_count** | **Integer** |  |  |
| **items** | [**Array&lt;CustomerCommunication&gt;**](CustomerCommunication.md) |  |  |
| **outbound_count** | **Integer** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ContactHistoryResponse.new(
  contact_id: null,
  inbound_count: null,
  items: null,
  outbound_count: null
)
```

