# SimplebillyApi::SupportTicketUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **assigned_to** | **String** |  | [optional] |
| **channel_id** | **String** |  | [optional] |
| **channel_type** | [**SupportChannelType**](SupportChannelType.md) |  | [optional] |
| **closed_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **customer_email** | **String** |  | [optional] |
| **customer_id** | **String** | References the customer entity. | [optional] |
| **customer_name** | **String** |  | [optional] |
| **external_id** | **String** |  | [optional] |
| **first_message_at** | **Time** |  | [optional] |
| **last_message_at** | **Time** |  | [optional] |
| **lead_id** | **String** | References the lead entity. | [optional] |
| **message_count** | **Integer** |  | [optional] |
| **order_ref** | **String** |  | [optional] |
| **priority** | [**TicketPriority**](TicketPriority.md) |  | [optional] |
| **resolution** | **String** |  | [optional] |
| **status** | [**SupportTicketStatus**](SupportTicketStatus.md) |  | [optional] |
| **subject** | **String** |  | [optional] |
| **tags** | **Object** |  | [optional] |
| **tenant_id** | **String** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::SupportTicketUpdate.new(
  assigned_to: null,
  channel_id: null,
  channel_type: null,
  closed_at: null,
  created_at: null,
  customer_email: null,
  customer_id: null,
  customer_name: null,
  external_id: null,
  first_message_at: null,
  last_message_at: null,
  lead_id: null,
  message_count: null,
  order_ref: null,
  priority: null,
  resolution: null,
  status: null,
  subject: null,
  tags: null,
  tenant_id: null,
  updated_at: null
)
```

