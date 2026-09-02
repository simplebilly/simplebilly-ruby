# SimplebillyApi::CreateTicketRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  | [optional] |
| **channel_type** | **String** |  | [optional] |
| **customer_email** | **String** |  | [optional] |
| **customer_id** | **String** |  | [optional] |
| **customer_name** | **String** |  | [optional] |
| **external_id** | **String** |  | [optional] |
| **message_body** | **String** |  |  |
| **order_ref** | **String** |  | [optional] |
| **subject** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CreateTicketRequest.new(
  channel_id: null,
  channel_type: null,
  customer_email: null,
  customer_id: null,
  customer_name: null,
  external_id: null,
  message_body: null,
  order_ref: null,
  subject: null
)
```

