# SimplebillyApi::VatSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **input_tax_items** | [**Array&lt;VatItem&gt;**](VatItem.md) |  |  |
| **output_tax_items** | [**Array&lt;VatItem&gt;**](VatItem.md) |  |  |
| **total_input_tax** | **String** |  |  |
| **total_output_tax** | **String** |  |  |
| **vat_due** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::VatSummary.new(
  input_tax_items: null,
  output_tax_items: null,
  total_input_tax: null,
  total_output_tax: null,
  vat_due: null
)
```

