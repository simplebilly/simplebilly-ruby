# SimplebillyApi::NewVersionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file_name** | **String** | Storage key of the already-uploaded bytes. |  |
| **file_size** | **Integer** |  | [optional] |
| **mime_type** | **String** |  | [optional] |
| **original_name** | **String** |  | [optional] |
| **sha256_hash** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::NewVersionRequest.new(
  file_name: null,
  file_size: null,
  mime_type: null,
  original_name: null,
  sha256_hash: null
)
```

