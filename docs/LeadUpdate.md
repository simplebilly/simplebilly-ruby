# SimplebillyApi::LeadUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company** | **String** |  | [optional] |
| **converted_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **email** | **String** |  | [optional] |
| **first_contact_at** | **Time** |  | [optional] |
| **name** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **score** | **Integer** |  | [optional] |
| **source** | **String** |  | [optional] |
| **status** | [**LeadStatus**](LeadStatus.md) |  | [optional] |
| **tags** | **Object** |  | [optional] |
| **tenant_id** | **String** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::LeadUpdate.new(
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

