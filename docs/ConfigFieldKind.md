# SimplebillyApi::ConfigFieldKind

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'simplebilly_api'

SimplebillyApi::ConfigFieldKind.openapi_one_of
# =>
# [
#   :'ConfigFieldKindOneOf',
#   :'ConfigFieldKindOneOf1',
#   :'ConfigFieldKindOneOf2',
#   :'ConfigFieldKindOneOf3',
#   :'ConfigFieldKindOneOf4'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'simplebilly_api'

SimplebillyApi::ConfigFieldKind.build(data)
# => #<ConfigFieldKindOneOf:0x00007fdd4aab02a0>

SimplebillyApi::ConfigFieldKind.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `ConfigFieldKindOneOf`
- `ConfigFieldKindOneOf1`
- `ConfigFieldKindOneOf2`
- `ConfigFieldKindOneOf3`
- `ConfigFieldKindOneOf4`
- `nil` (if no type matches)

