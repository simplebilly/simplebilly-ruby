# SimplebillyApi::InstituteProfile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institute_type** | [**InstituteType**](InstituteType.md) | Institutsart: \&quot;kein\&quot; | \&quot;kreditinstitut\&quot; | \&quot;finanzdienstleistungsinstitut\&quot; | \&quot;finanzunternehmen\&quot; | \&quot;versicherung\&quot;. | [optional] |
| **kapitalmarktorientiert** | **Boolean** | Kapitalmarktorientierung (§ 325 Abs. 4 HGB): Offenlegungsfrist 4 statt 12 Monate. | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::InstituteProfile.new(
  institute_type: null,
  kapitalmarktorientiert: null
)
```

