# SimplebillyApi::UmsatzsteuerReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **generated_at** | **String** |  |  |
| **input_tax** | [**Array&lt;VatDetail&gt;**](VatDetail.md) |  |  |
| **output_tax** | [**Array&lt;VatDetail&gt;**](VatDetail.md) |  |  |
| **period** | **String** |  |  |
| **total_input_tax** | **String** |  |  |
| **total_output_tax** | **String** |  |  |
| **vat_payable** | **String** |  |  |
| **vat_refund** | **String** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::UmsatzsteuerReport.new(
  generated_at: null,
  input_tax: null,
  output_tax: null,
  period: null,
  total_input_tax: null,
  total_output_tax: null,
  vat_payable: null,
  vat_refund: null
)
```

