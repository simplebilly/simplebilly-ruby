# SimplebillyApi::AttachmentVersion

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attachment_id** | **String** | Parent attachment whose history this row records. |  |
| **file_name** | **String** | Storage key of this version&#39;s bytes. |  |
| **file_size** | **Integer** |  | [optional] |
| **mime_type** | **String** |  | [optional] |
| **original_name** | **String** |  | [optional] |
| **sha256_hash** | **String** |  | [optional] |
| **uploaded_by** | **String** |  | [optional] |
| **version_number** | **Integer** | 1-based; ascending per attachment in upload order. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AttachmentVersion.new(
  attachment_id: null,
  file_name: null,
  file_size: null,
  mime_type: null,
  original_name: null,
  sha256_hash: null,
  uploaded_by: null,
  version_number: null
)
```

