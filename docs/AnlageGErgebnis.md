# SimplebillyApi::AnlageGErgebnis

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gewinn_verlust** | **String** |  |  |
| **gewst_gezahlt** | **String** |  |  |
| **gewst_messbetrag_approx** | **String** |  |  |
| **gewst_pflichtig** | **Boolean** |  |  |
| **jahr** | **Integer** |  |  |
| **kfz_hinweise** | [**Array&lt;AnlageGKfzHinweis&gt;**](AnlageGKfzHinweis.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::AnlageGErgebnis.new(
  gewinn_verlust: null,
  gewst_gezahlt: null,
  gewst_messbetrag_approx: null,
  gewst_pflichtig: null,
  jahr: null,
  kfz_hinweise: null
)
```

