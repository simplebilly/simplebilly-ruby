# SimplebillyApi::Activity

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_type** | [**ActivityType**](ActivityType.md) | One of: call | email | meeting | task | note |  |
| **assigned_to** | **String** | User responsible (&#x60;employee.employee_id&#x60;). | [optional] |
| **contact_id** | **String** | Contact this activity belongs to (&#x60;contact.contact_id&#x60;). References the contact entity. | [optional] |
| **description** | **String** |  | [optional] |
| **due_date** | **Date** | Follow-up / Wiedervorlage date. Open activities with a due date in the past are overdue. | [optional] |
| **reminder_date** | **Date** | When to remind about the follow-up. | [optional] |
| **status** | [**ActivityStatus**](ActivityStatus.md) | One of: open | done | cancelled |  |
| **subject** | **String** | Short subject line. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Activity.new(
  activity_type: null,
  assigned_to: null,
  contact_id: null,
  description: null,
  due_date: null,
  reminder_date: null,
  status: null,
  subject: null
)
```

