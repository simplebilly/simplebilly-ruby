# SimplebillyApi::ContactCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_holder** | **String** |  | [optional] |
| **acquisition_cost** | **String** |  | [optional] |
| **address_supplement** | **String** |  | [optional] |
| **attention** | **String** |  | [optional] |
| **bank_name** | **String** |  | [optional] |
| **bic** | **String** |  | [optional] |
| **buyer_reference** | **String** |  | [optional] |
| **category** | **String** |  | [optional] |
| **certificate_authority** | **String** |  | [optional] |
| **certificate_number** | **String** |  | [optional] |
| **certificate_paragraph** | **String** |  | [optional] |
| **certificate_valid_until** | **Date** |  | [optional] |
| **city** | **String** |  | [optional] |
| **company_name** | **String** |  | [optional] |
| **contact_persons** | **Object** |  | [optional] |
| **contact_type** | [**ContactType**](ContactType.md) |  |  |
| **country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **credit_limit** | **String** |  | [optional] |
| **creditor_account_skr03** | **String** |  | [optional] |
| **creditor_account_skr04** | **String** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **custom_fields** | **Object** |  | [optional] |
| **customer_number** | **String** |  | [optional] |
| **debitor_account_skr03** | **String** |  | [optional] |
| **debitor_account_skr04** | **String** |  | [optional] |
| **default_debitor_number** | **String** |  | [optional] |
| **delivery_block** | **Boolean** |  | [optional] |
| **department** | **String** |  | [optional] |
| **discount_days** | **Integer** |  | [optional] |
| **discount_percentage** | **String** |  | [optional] |
| **donation_receipt_eligible** | **Boolean** |  | [optional] |
| **email** | **String** |  | [optional] |
| **external_id** | **String** |  | [optional] |
| **fax** | **String** |  | [optional] |
| **iban** | **String** |  | [optional] |
| **industry** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **is_member** | **Boolean** |  | [optional] |
| **is_nonprofit** | **Boolean** |  | [optional] |
| **last_contact_date** | **Date** |  | [optional] |
| **last_purchase_date** | **Date** |  | [optional] |
| **leitweg_id** | **String** |  | [optional] |
| **lifetime_value** | **String** |  | [optional] |
| **mandate_date** | **Date** |  | [optional] |
| **mandate_reference** | **String** |  | [optional] |
| **marketing_consent** | **Boolean** |  | [optional] |
| **marketing_consent_at** | **Time** |  | [optional] |
| **marketing_consent_source** | **String** |  | [optional] |
| **mobile** | **String** |  | [optional] |
| **name** | **String** |  |  |
| **next_contact_date** | **Date** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **opening_balance** | **String** |  | [optional] |
| **opening_balance_date** | **Date** |  | [optional] |
| **order_reference** | **String** |  | [optional] |
| **payment_block** | **Boolean** |  | [optional] |
| **payment_grace_period_days** | **Integer** |  | [optional] |
| **payment_methods** | **Array&lt;String&gt;** |  | [optional] |
| **payment_terms** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **rating** | **Integer** |  | [optional] |
| **sales_representative** | **String** |  | [optional] |
| **sepa_batch_booking** | **Boolean** |  | [optional] |
| **sepa_sequence_type** | [**SepaSequenceType**](SepaSequenceType.md) |  | [optional] |
| **social_media** | **Object** |  | [optional] |
| **source** | **String** |  | [optional] |
| **state** | **String** |  | [optional] |
| **street** | **String** |  | [optional] |
| **street_number** | **String** |  | [optional] |
| **supplier_number** | **String** |  | [optional] |
| **tags** | **Array&lt;String&gt;** |  | [optional] |
| **tax_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **tax_number** | **String** |  | [optional] |
| **tax_office** | **String** |  | [optional] |
| **total_invoices** | **Integer** |  | [optional] |
| **total_revenue** | **String** |  | [optional] |
| **vat_id** | **String** |  | [optional] |
| **vat_id_validated** | **Boolean** |  | [optional] |
| **vat_id_validation_date** | **Date** |  | [optional] |
| **website** | **String** |  | [optional] |
| **zip** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ContactCreate.new(
  account_holder: null,
  acquisition_cost: null,
  address_supplement: null,
  attention: null,
  bank_name: null,
  bic: null,
  buyer_reference: null,
  category: null,
  certificate_authority: null,
  certificate_number: null,
  certificate_paragraph: null,
  certificate_valid_until: null,
  city: null,
  company_name: null,
  contact_persons: null,
  contact_type: null,
  country: null,
  credit_limit: null,
  creditor_account_skr03: null,
  creditor_account_skr04: null,
  currency: null,
  custom_fields: null,
  customer_number: null,
  debitor_account_skr03: null,
  debitor_account_skr04: null,
  default_debitor_number: null,
  delivery_block: null,
  department: null,
  discount_days: null,
  discount_percentage: null,
  donation_receipt_eligible: null,
  email: null,
  external_id: null,
  fax: null,
  iban: null,
  industry: null,
  is_active: null,
  is_member: null,
  is_nonprofit: null,
  last_contact_date: null,
  last_purchase_date: null,
  leitweg_id: null,
  lifetime_value: null,
  mandate_date: null,
  mandate_reference: null,
  marketing_consent: null,
  marketing_consent_at: null,
  marketing_consent_source: null,
  mobile: null,
  name: null,
  next_contact_date: null,
  notes: null,
  opening_balance: null,
  opening_balance_date: null,
  order_reference: null,
  payment_block: null,
  payment_grace_period_days: null,
  payment_methods: null,
  payment_terms: null,
  phone: null,
  rating: null,
  sales_representative: null,
  sepa_batch_booking: null,
  sepa_sequence_type: null,
  social_media: null,
  source: null,
  state: null,
  street: null,
  street_number: null,
  supplier_number: null,
  tags: null,
  tax_country: null,
  tax_number: null,
  tax_office: null,
  total_invoices: null,
  total_revenue: null,
  vat_id: null,
  vat_id_validated: null,
  vat_id_validation_date: null,
  website: null,
  zip: null
)
```

