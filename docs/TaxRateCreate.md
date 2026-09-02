# SimplebillyApi::TaxRateCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **String** | ISO 3166-1 alpha-2 country code. |  |
| **effective_from** | **Date** | Date this rate took effect; &#x60;None&#x60; &#x3D; not date-bound. | [optional] |
| **is_default** | **Boolean** | Default rate for the country (one per country); fallback for lookups when no dated rate applies. |  |
| **name** | **String** | Human name, e.g. \&quot;VAT\&quot;. |  |
| **rate_percent** | **Integer** | Rate in hundredths of a percent: 1900 &#x3D; 19.00%. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::TaxRateCreate.new(
  country_code: null,
  effective_from: null,
  is_default: null,
  name: null,
  rate_percent: null
)
```

