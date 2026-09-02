# SimplebillyApi::PluginError

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'simplebilly_api'

SimplebillyApi::PluginError.openapi_one_of
# =>
# [
#   :'PluginErrorOneOf',
#   :'PluginErrorOneOf1',
#   :'PluginErrorOneOf2',
#   :'PluginErrorOneOf3',
#   :'PluginErrorOneOf4',
#   :'PluginErrorOneOf5',
#   :'PluginErrorOneOf6'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'simplebilly_api'

SimplebillyApi::PluginError.build(data)
# => #<PluginErrorOneOf:0x00007fdd4aab02a0>

SimplebillyApi::PluginError.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `PluginErrorOneOf`
- `PluginErrorOneOf1`
- `PluginErrorOneOf2`
- `PluginErrorOneOf3`
- `PluginErrorOneOf4`
- `PluginErrorOneOf5`
- `PluginErrorOneOf6`
- `nil` (if no type matches)

