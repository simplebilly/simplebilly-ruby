# SimplebillyApi::PlatformInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **author** | **String** |  |  |
| **changelog** | [**Array&lt;ChangelogEntry&gt;**](ChangelogEntry.md) |  |  |
| **config_field_names** | **Array&lt;String&gt;** |  |  |
| **config_fields** | [**Array&lt;ConfigFieldInfo&gt;**](ConfigFieldInfo.md) |  |  |
| **display_name** | **String** |  |  |
| **platform** | **String** |  |  |
| **pricing** | [**PluginPricing**](PluginPricing.md) |  |  |
| **supported_entities** | **Array&lt;String&gt;** |  |  |
| **supports_export** | **Boolean** |  |  |
| **supports_import** | **Boolean** |  |  |
| **supports_oauth** | **Boolean** |  |  |
| **version** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PlatformInfo.new(
  author: null,
  changelog: null,
  config_field_names: null,
  config_fields: null,
  display_name: null,
  platform: null,
  pricing: null,
  supported_entities: null,
  supports_export: null,
  supports_import: null,
  supports_oauth: null,
  version: null
)
```

