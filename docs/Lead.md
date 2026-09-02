# SimplebillyApi::Lead

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company** | **String** |  | [optional] |
| **converted_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  |  |
| **email** | **String** |  | [optional] |
| **first_contact_at** | **Time** |  |  |
| **name** | **String** |  |  |
| **notes** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **score** | **Integer** |  |  |
| **source** | **String** |  |  |
| **status** | [**LeadStatus**](LeadStatus.md) |  |  |
| **tags** | **Object** |  |  |
| **tenant_id** | **String** |  |  |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Lead.new(
  company: null,
  converted_at: null,
  created_at: null,
  email: null,
  first_contact_at: null,
  name: null,
  notes: null,
  phone: null,
  score: null,
  source: null,
  status: null,
  tags: null,
  tenant_id: null,
  updated_at: null
)
```

