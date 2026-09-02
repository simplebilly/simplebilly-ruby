# SimplebillyApi::PostingCategory

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_number** | **String** |  | [optional] |
| **account_number_skr03** | **String** |  | [optional] |
| **account_number_skr04** | **String** |  | [optional] |
| **account_number_skr49** | **String** |  | [optional] |
| **category_id** | **String** |  |  |
| **default_vat_rate** | **Integer** |  |  |
| **description** | **String** |  | [optional] |
| **eks_category** | **String** |  | [optional] |
| **is_active** | **Boolean** |  |  |
| **is_system** | **Boolean** |  |  |
| **name** | **String** |  |  |
| **skr_version** | **String** |  |  |
| **type** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PostingCategory.new(
  account_number: null,
  account_number_skr03: null,
  account_number_skr04: null,
  account_number_skr49: null,
  category_id: null,
  default_vat_rate: null,
  description: null,
  eks_category: null,
  is_active: null,
  is_system: null,
  name: null,
  skr_version: null,
  type: null
)
```

