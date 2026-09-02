# SimplebillyApi::InvoiceCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attachments** | **Object** |  | [optional] |
| **billing_period_end** | **Date** |  | [optional] |
| **billing_period_start** | **Date** |  | [optional] |
| **cancellation_date** | **Date** |  | [optional] |
| **cancellation_invoice_id** | **String** | References the invoice entity. | [optional] |
| **cancellation_reason** | **String** |  | [optional] |
| **contract_id** | **String** | References the contract entity. | [optional] |
| **currency** | [**CurrencyCode**](CurrencyCode.md) |  |  |
| **customer_id** | **String** | References the customer entity. | [optional] |
| **discount_amount** | **String** |  | [optional] |
| **discount_days** | **Integer** |  | [optional] |
| **discount_percentage** | **String** |  | [optional] |
| **document_type** | [**DocumentType**](DocumentType.md) |  | [optional] |
| **dunning_level** | **Integer** |  | [optional] |
| **input_vat_amount** | **String** |  | [optional] |
| **input_vat_deductible** | **Boolean** |  | [optional] |
| **input_vat_percentage** | **String** |  | [optional] |
| **introduction_text** | **String** |  | [optional] |
| **invoice_type** | [**InvoiceType**](InvoiceType.md) |  |  |
| **is_cancelled** | **Boolean** |  | [optional] |
| **is_draft** | **Boolean** |  | [optional] |
| **is_eu_acquisition** | **Boolean** |  | [optional] |
| **is_eu_delivery** | **Boolean** |  | [optional] |
| **is_intra_community_acquisition** | **Boolean** |  | [optional] |
| **is_reverse_charge** | **Boolean** |  | [optional] |
| **issue_date** | **Date** |  |  |
| **ledger_account** | **String** |  | [optional] |
| **line_items** | **Object** |  |  |
| **margin25a** | **Boolean** |  | [optional] |
| **margin25a_gross** | **String** |  | [optional] |
| **margin25a_purchase_price** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **order_number** | **String** |  | [optional] |
| **original_pdf_path** | **String** |  | [optional] |
| **paid_amount** | **String** |  | [optional] |
| **payment_due_date** | **Date** |  | [optional] |
| **payment_status** | [**PaymentStatus**](PaymentStatus.md) |  | [optional] |
| **payment_terms_text** | **String** |  | [optional] |
| **preceding_sales_voucher_id** | **String** | References the preceding sales voucher entity. | [optional] |
| **preceding_sales_voucher_type** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] |
| **receipt_confirmation_available** | **Boolean** |  | [optional] |
| **related_invoice_id** | **String** | References the invoice entity. | [optional] |
| **relationship_type** | **String** |  | [optional] |
| **sender_snapshot** | **Object** |  | [optional] |
| **sent_at** | **Time** |  | [optional] |
| **service_period_end** | **Date** |  | [optional] |
| **service_period_start** | **Date** |  | [optional] |
| **status** | [**InvoiceStatus**](InvoiceStatus.md) |  |  |
| **subtotal** | **String** |  |  |
| **supplier_id** | **String** | References the supplier entity. | [optional] |
| **tax_exemption_reason** | **String** |  | [optional] |
| **total_amount** | **String** |  |  |
| **total_tax** | **String** |  |  |
| **vat_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **vat_special_case** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::InvoiceCreate.new(
  attachments: null,
  billing_period_end: null,
  billing_period_start: null,
  cancellation_date: null,
  cancellation_invoice_id: null,
  cancellation_reason: null,
  contract_id: null,
  currency: null,
  customer_id: null,
  discount_amount: null,
  discount_days: null,
  discount_percentage: null,
  document_type: null,
  dunning_level: null,
  input_vat_amount: null,
  input_vat_deductible: null,
  input_vat_percentage: null,
  introduction_text: null,
  invoice_type: null,
  is_cancelled: null,
  is_draft: null,
  is_eu_acquisition: null,
  is_eu_delivery: null,
  is_intra_community_acquisition: null,
  is_reverse_charge: null,
  issue_date: null,
  ledger_account: null,
  line_items: null,
  margin25a: null,
  margin25a_gross: null,
  margin25a_purchase_price: null,
  notes: null,
  order_number: null,
  original_pdf_path: null,
  paid_amount: null,
  payment_due_date: null,
  payment_status: null,
  payment_terms_text: null,
  preceding_sales_voucher_id: null,
  preceding_sales_voucher_type: null,
  receipt_confirmation_available: null,
  related_invoice_id: null,
  relationship_type: null,
  sender_snapshot: null,
  sent_at: null,
  service_period_end: null,
  service_period_start: null,
  status: null,
  subtotal: null,
  supplier_id: null,
  tax_exemption_reason: null,
  total_amount: null,
  total_tax: null,
  vat_country: null,
  vat_special_case: null
)
```

