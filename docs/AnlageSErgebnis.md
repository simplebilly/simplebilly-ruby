# SimplebillyApi::AnlageSErgebnis

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gewinn_verlust** | **String** |  |  |
| **jahr** | **Integer** |  |  |
| **kfz_hinweise** | [**Array&lt;AnlageSKfzHinweis&gt;**](AnlageSKfzHinweis.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AnlageSErgebnis.new(
  gewinn_verlust: null,
  jahr: null,
  kfz_hinweise: null
)
```

