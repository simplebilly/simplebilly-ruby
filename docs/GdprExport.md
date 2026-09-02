# SimplebillyApi::GdprExport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_log** | [**Array&lt;GdprActivity&gt;**](GdprActivity.md) |  |  |
| **api_keys** | [**Array&lt;GdprApiKey&gt;**](GdprApiKey.md) | Key identifiers and names only — never a usable credential. |  |
| **billing** | [**Array&lt;GdprBillingInfo&gt;**](GdprBillingInfo.md) |  |  |
| **exported_at** | **Time** |  |  |
| **generated_by_ai** | **Boolean** | Honesty field: this document is a plain data dump, never AI-generated. |  |
| **notifications** | [**Array&lt;GdprNotification&gt;**](GdprNotification.md) |  |  |
| **refresh_tokens** | [**Array&lt;GdprRefreshToken&gt;**](GdprRefreshToken.md) | Session records: metadata only, never the token hash. |  |
| **tenants** | [**Array&lt;GdprTenant&gt;**](GdprTenant.md) |  |  |
| **usage_events** | [**Array&lt;GdprUsageEvent&gt;**](GdprUsageEvent.md) |  |  |
| **user** | [**GdprUser**](GdprUser.md) |  |  |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::GdprExport.new(
  activity_log: null,
  api_keys: null,
  billing: null,
  exported_at: null,
  generated_by_ai: null,
  notifications: null,
  refresh_tokens: null,
  tenants: null,
  usage_events: null,
  user: null
)
```

