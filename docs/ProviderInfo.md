# SimplebillyApi::ProviderInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **display_name** | **String** |  |  |
| **name** | **String** |  |  |
| **requires_api_key** | **Boolean** |  |  |
| **services** | **Array&lt;String&gt;** |  |  |
| **supports_label_creation** | **Boolean** |  |  |
| **supports_rate_estimation** | **Boolean** |  |  |
| **supports_tracking** | **Boolean** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProviderInfo.new(
  display_name: null,
  name: null,
  requires_api_key: null,
  services: null,
  supports_label_creation: null,
  supports_rate_estimation: null,
  supports_tracking: null
)
```

