# SimplebillyApi::EBilanzReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_overview** | [**Array&lt;AccountOverview&gt;**](AccountOverview.md) |  |  |
| **balance_sheet** | [**BalanceSheet**](BalanceSheet.md) |  |  |
| **generated_at** | **String** |  |  |
| **income_statement** | [**IncomeStatement**](IncomeStatement.md) |  |  |
| **period** | **String** |  |  |
| **vat_summary** | [**VatSummary**](VatSummary.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::EBilanzReport.new(
  account_overview: null,
  balance_sheet: null,
  generated_at: null,
  income_statement: null,
  period: null,
  vat_summary: null
)
```

