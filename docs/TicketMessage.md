# SimplebillyApi::TicketMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **author_email** | **String** |  | [optional] |
| **author_name** | **String** |  | [optional] |
| **body** | **String** |  |  |
| **body_html** | **String** |  | [optional] |
| **channel_id** | **String** |  | [optional] |
| **created_at** | **Time** |  |  |
| **direction** | [**MessageDirection**](MessageDirection.md) |  |  |
| **external_id** | **String** |  | [optional] |
| **is_internal** | **Boolean** |  |  |
| **message_type** | [**MessageType**](MessageType.md) |  |  |
| **metadata** | **Object** |  |  |
| **tenant_id** | **String** |  |  |
| **ticket_id** | **String** | References the ticket entity. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TicketMessage.new(
  author_email: null,
  author_name: null,
  body: null,
  body_html: null,
  channel_id: null,
  created_at: null,
  direction: null,
  external_id: null,
  is_internal: null,
  message_type: null,
  metadata: null,
  tenant_id: null,
  ticket_id: null
)
```

