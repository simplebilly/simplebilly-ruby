# SimplebillyApi::InvoiceLineItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **article_number** | **String** |  | [optional] |
| **description** | **String** |  |  |
| **discount_amount** | **String** |  | [optional] |
| **discount_percentage** | **String** |  | [optional] |
| **input_vat_deductible** | **Boolean** |  | [optional] |
| **input_vat_rate** | **String** |  | [optional] |
| **is_intra_community_acquisition** | **Boolean** |  | [optional] |
| **is_margin_25a** | **Boolean** |  | [optional] |
| **ledger_account** | **String** |  | [optional] |
| **line_total** | **String** |  |  |
| **line_total_gross** | **String** |  | [optional] |
| **margin_25a_purchase_price** | **String** |  | [optional] |
| **meter_point_id** | **String** |  | [optional] |
| **position** | **Integer** |  |  |
| **price_components** | **Object** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **product_sku** | **String** |  | [optional] |
| **quantity** | **String** |  |  |
| **supplier_article_number** | **String** |  | [optional] |
| **tax_rate** | **String** |  | [optional] |
| **unit** | **Object** |  |  |
| **unit_price** | **String** |  |  |
| **usage_data_id** | **String** |  | [optional] |
| **vat_rate_nominal** | **String** |  | [optional] |
| **vat_special_case** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::InvoiceLineItem.new(
  article_number: null,
  description: Electricity Work Price,
  discount_amount: null,
  discount_percentage: null,
  input_vat_deductible: null,
  input_vat_rate: null,
  is_intra_community_acquisition: null,
  is_margin_25a: null,
  ledger_account: null,
  line_total: 19.9,
  line_total_gross: null,
  margin_25a_purchase_price: null,
  meter_point_id: null,
  position: null,
  price_components: null,
  product_id: null,
  product_sku: null,
  quantity: 10.0,
  supplier_article_number: null,
  tax_rate: 19.0,
  unit: null,
  unit_price: 1.99,
  usage_data_id: null,
  vat_rate_nominal: null,
  vat_special_case: null
)
```

