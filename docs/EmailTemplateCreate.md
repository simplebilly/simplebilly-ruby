# SimplebillyApi::EmailTemplateCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **String** | E-mail body with optional placeholders. |  |
| **name** | **String** | Human-readable template name, e.g. \&quot;Follow-up after quote\&quot;. |  |
| **status** | [**EmailTemplateStatus**](EmailTemplateStatus.md) | One of: active | inactive |  |
| **subject** | **String** | E-mail subject line with optional placeholders. |  |
| **variables** | **Object** | Placeholders used by this template, e.g. &#x60;[\&quot;contact.first_name\&quot;]&#x60;. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EmailTemplateCreate.new(
  body: null,
  name: null,
  status: null,
  subject: null,
  variables: null
)
```

