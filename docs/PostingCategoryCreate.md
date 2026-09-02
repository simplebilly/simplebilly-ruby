# SimplebillyApi::PostingCategoryCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_number** | **String** |  | [optional] |
| **account_number_skr03** | **String** |  | [optional] |
| **account_number_skr04** | **String** |  | [optional] |
| **account_number_skr49** | **String** |  | [optional] |
| **category_type** | [**PostingCategoryType**](PostingCategoryType.md) |  |  |
| **created_at** | **Time** |  |  |
| **default_vat_rate** | **Integer** |  |  |
| **description** | **String** |  | [optional] |
| **eks_category** | **String** |  | [optional] |
| **eu_vat_line** | **Integer** |  | [optional] |
| **input_vat_percentage** | **String** |  |  |
| **is_active** | **Boolean** |  |  |
| **is_system** | **Boolean** |  |  |
| **name** | **String** |  |  |
| **skr_version** | **String** |  |  |
| **updated_at** | **Time** |  | [optional] |
| **user_modified_skr03** | **Boolean** |  |  |
| **user_modified_skr04** | **Boolean** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::PostingCategoryCreate.new(
  account_number: null,
  account_number_skr03: null,
  account_number_skr04: null,
  account_number_skr49: null,
  category_type: null,
  created_at: null,
  default_vat_rate: null,
  description: null,
  eks_category: null,
  eu_vat_line: null,
  input_vat_percentage: null,
  is_active: null,
  is_system: null,
  name: null,
  skr_version: null,
  updated_at: null,
  user_modified_skr03: null,
  user_modified_skr04: null
)
```

