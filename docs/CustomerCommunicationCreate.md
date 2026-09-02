# SimplebillyApi::CustomerCommunicationCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **String** | The message body, call summary or note text. | [optional] |
| **channel** | [**CommunicationChannel**](CommunicationChannel.md) |  |  |
| **contact_id** | **String** | The contact (customer/supplier) this communication belongs to. References the contact entity. |  |
| **counterparty** | **String** | Email/phone of the counterparty, if applicable. | [optional] |
| **direction** | [**CommunicationDirection**](CommunicationDirection.md) |  |  |
| **occurred_at** | **Time** | When the communication happened (defaults to now on create). | [optional] |
| **subject** | **String** |  | [optional] |
| **tags** | **Object** | Free-form tags, e.g. &#x60;[\&quot;follow-up-required\&quot;]&#x60;. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CustomerCommunicationCreate.new(
  body: null,
  channel: null,
  contact_id: null,
  counterparty: null,
  direction: null,
  occurred_at: null,
  subject: null,
  tags: null
)
```

