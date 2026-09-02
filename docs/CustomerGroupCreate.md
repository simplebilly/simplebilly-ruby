# SimplebillyApi::CustomerGroupCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** |  | [optional] |
| **member_ids** | **Array&lt;String&gt;** | Contact ids that are members of this group. | [optional] |
| **membership_filter** | **String** | Rule description for membership, e.g. \&quot;orders &gt; 5 last 12 months\&quot;. | [optional] |
| **name** | **String** | Unique group name, e.g. \&quot;VIP\&quot;, \&quot;Wholesale\&quot;, \&quot;Newsletter\&quot;. |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::CustomerGroupCreate.new(
  description: null,
  member_ids: null,
  membership_filter: null,
  name: null
)
```

