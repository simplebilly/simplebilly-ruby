# SimplebillyApi::WarehouseUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address_city** | **String** |  | [optional] |
| **address_country** | [**CountryCode**](CountryCode.md) |  | [optional] |
| **address_street** | **String** |  | [optional] |
| **address_zip** | **String** |  | [optional] |
| **bin_locations** | **Object** | JSON array of bin locations, e.g. &#x60;[\&quot;A-01-01\&quot;, \&quot;A-01-02\&quot;]&#x60;. | [optional] |
| **code** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **is_default** | **Boolean** |  | [optional] |
| **name** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::WarehouseUpdate.new(
  address_city: null,
  address_country: null,
  address_street: null,
  address_zip: null,
  bin_locations: null,
  code: null,
  is_active: null,
  is_default: null,
  name: null,
  notes: null
)
```

