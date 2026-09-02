# SimplebillyApi::PluginPricing

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'simplebilly_api'

SimplebillyApi::PluginPricing.openapi_one_of
# =>
# [
#   :'PluginPricingOneOf',
#   :'PluginPricingOneOf1',
#   :'PluginPricingOneOf2'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'simplebilly_api'

SimplebillyApi::PluginPricing.build(data)
# => #<PluginPricingOneOf:0x00007fdd4aab02a0>

SimplebillyApi::PluginPricing.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `PluginPricingOneOf`
- `PluginPricingOneOf1`
- `PluginPricingOneOf2`
- `nil` (if no type matches)

