# SimplebillyApi::ProductUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **availability** | **String** |  | [optional] |
| **barcode** | **String** |  | [optional] |
| **brand** | **String** |  | [optional] |
| **category_id** | **String** |  | [optional] |
| **condition** | **String** |  | [optional] |
| **default_ledger_account** | **String** |  | [optional] |
| **default_price** | **String** |  | [optional] |
| **default_price_formula_id** | **String** | References the price formula entity. | [optional] |
| **default_tax_rate** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **gtin** | **String** |  | [optional] |
| **height** | **String** |  | [optional] |
| **image_link** | **String** |  | [optional] |
| **images** | **Object** |  | [optional] |
| **is_taxable** | **Boolean** |  | [optional] |
| **length** | **String** |  | [optional] |
| **link** | **String** |  | [optional] |
| **max_stock** | **Integer** | Target stock level used by reorder proposals. | [optional] |
| **min_stock** | **Integer** | Reorder point — when stock falls below this, a reorder is suggested. | [optional] |
| **mpn** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **package_height** | **String** |  | [optional] |
| **package_length** | **String** |  | [optional] |
| **package_weight_unit** | **String** |  | [optional] |
| **package_weight_value** | **String** |  | [optional] |
| **package_width** | **String** |  | [optional] |
| **product_code** | **String** |  | [optional] |
| **product_type** | **String** |  | [optional] |
| **purchase_price** | **String** |  | [optional] |
| **reorder_quantity** | **Integer** | Suggested purchase quantity when a reorder proposal is created. | [optional] |
| **sale_price** | **String** |  | [optional] |
| **shipping_price** | **String** |  | [optional] |
| **shipping_requires_insurance** | **Boolean** |  | [optional] |
| **sku** | **String** |  | [optional] |
| **stock_quantity** | **Integer** |  | [optional] |
| **tags** | **Object** |  | [optional] |
| **tax_price** | **String** |  | [optional] |
| **track_batch** | **Boolean** | Whether this product requires batch (Chargennummer) tracking. | [optional] |
| **track_serial** | **Boolean** | Whether this product requires serial-number tracking. | [optional] |
| **unit** | **Object** |  | [optional] |
| **weight_unit** | **String** |  | [optional] |
| **weight_value** | **String** |  | [optional] |
| **width** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ProductUpdate.new(
  availability: null,
  barcode: null,
  brand: null,
  category_id: null,
  condition: null,
  default_ledger_account: null,
  default_price: null,
  default_price_formula_id: null,
  default_tax_rate: null,
  description: null,
  gtin: null,
  height: null,
  image_link: null,
  images: null,
  is_taxable: null,
  length: null,
  link: null,
  max_stock: null,
  min_stock: null,
  mpn: null,
  name: null,
  package_height: null,
  package_length: null,
  package_weight_unit: null,
  package_weight_value: null,
  package_width: null,
  product_code: null,
  product_type: null,
  purchase_price: null,
  reorder_quantity: null,
  sale_price: null,
  shipping_price: null,
  shipping_requires_insurance: null,
  sku: null,
  stock_quantity: null,
  tags: null,
  tax_price: null,
  track_batch: null,
  track_serial: null,
  unit: null,
  weight_unit: null,
  weight_value: null,
  width: null
)
```

