# SimplebillyApi::Attachment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** | Contact this attachment belongs to (per-contact DMS). References the contact entity. | [optional] |
| **file_name** | **String** |  |  |
| **file_size** | **Integer** |  | [optional] |
| **mime_type** | **String** |  | [optional] |
| **ocr_text** | **String** | Raw text extracted by client-side OCR (tesseract.js), if run. | [optional] |
| **original_name** | **String** |  |  |
| **pdfa_path** | **String** |  | [optional] |
| **sha256_hash** | **String** |  | [optional] |
| **uploaded_by** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Attachment.new(
  contact_id: null,
  file_name: null,
  file_size: null,
  mime_type: null,
  ocr_text: null,
  original_name: null,
  pdfa_path: null,
  sha256_hash: null,
  uploaded_by: null
)
```

