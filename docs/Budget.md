# SimplebillyApi::Budget

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category** | **String** | Posting category key (matches &#x60;category&#x60; on journal entries). |  |
| **monthly_goal** | **String** | Monthly goal amount (gross). 0 means \&quot;no goal set\&quot;. |  |
| **updated_at** | **Time** |  | [optional] |
| **year** | **Integer** | Budget year the goal applies to. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Budget.new(
  category: null,
  monthly_goal: null,
  updated_at: null,
  year: null
)
```

