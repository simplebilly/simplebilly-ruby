# SimplebillyApi::ShippingRate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **breakdown** | **String** |  | [optional] |
| **carrier** | **String** |  |  |
| **cross_border_surcharge** | **String** |  | [optional] |
| **destination_country** | **String** | ISO-2 code of destination country. |  |
| **estimated_days** | **Integer** |  | [optional] |
| **from_api** | **Boolean** | True when the rate was obtained via an API call rather than calculation. |  |
| **insured_value** | **String** |  | [optional] |
| **island_surcharge** | **String** |  | [optional] |
| **origin_country** | **String** | ISO-2 code of origin country. |  |
| **rate** | **String** |  |  |
| **service** | **String** |  |  |
| **volume_discount** | **String** |  | [optional] |
| **weight_kg** | **Float** |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::ShippingRate.new(
  breakdown: null,
  carrier: null,
  cross_border_surcharge: null,
  destination_country: null,
  estimated_days: null,
  from_api: null,
  insured_value: null,
  island_surcharge: null,
  origin_country: null,
  rate: null,
  service: null,
  volume_discount: null,
  weight_kg: null
)
```

