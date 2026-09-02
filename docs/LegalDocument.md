# SimplebillyApi::LegalDocument

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** | Plain text, &#x60;\\n\\n&#x60; separates paragraphs. |  |
| **doc_type** | [**LegalDocType**](LegalDocType.md) |  |  |
| **lang** | [**LanguageCode**](LanguageCode.md) |  |  |
| **title** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::LegalDocument.new(
  content: null,
  doc_type: null,
  lang: null,
  title: null
)
```

