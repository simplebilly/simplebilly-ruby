# SimplebillyApi::BillingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_plans**](BillingApi.md#get_plans) | **GET** /api/v1/plans | All canonical plans (free/starter/business/enterprise) — the single source of truth lives in &#x60;crate::saasy::plans&#x60;, matching marketing. |
| [**get_quota_api**](BillingApi.md#get_quota_api) | **GET** /api/v1/quota | Effective limits + current usage for the calling tenant. |
| [**get_subscription_api**](BillingApi.md#get_subscription_api) | **GET** /api/v1/subscription |  |
| [**get_usage_api**](BillingApi.md#get_usage_api) | **GET** /api/v1/usage |  |
| [**paddle_subscription_webhook**](BillingApi.md#paddle_subscription_webhook) | **POST** /api/webhooks/paddle/subscription | Paddle Billing subscription webhook. Verifies the &#x60;Paddle-Signature&#x60; header (HMAC-SHA256 over &#x60;\&quot;{ts}:{raw_body}\&quot;&#x60; with the webhook secret), then updates &#x60;billing_info&#x60; and &#x60;tenants.plan&#x60; for the tenant identified by the subscription &#x60;custom_data&#x60; (JSON &#x60;{\&quot;tenant_id\&quot;: \&quot;...\&quot;}&#x60; or a bare tenant UUID). |
| [**put_quota_api**](BillingApi.md#put_quota_api) | **PUT** /api/v1/quota | Write the per-tenant quota override (&#x60;admin:settings&#x60;). An empty object clears the override. |


## get_plans

> <ApiResponseVecPlan> get_plans

All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BillingApi.new

begin
  # All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.
  result = api_instance.get_plans
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_plans: #{e}"
end
```

#### Using the get_plans_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseVecPlan>, Integer, Hash)> get_plans_with_http_info

```ruby
begin
  # All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.
  data, status_code, headers = api_instance.get_plans_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseVecPlan>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_plans_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiResponseVecPlan**](ApiResponseVecPlan.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_quota_api

> get_quota_api

Effective limits + current usage for the calling tenant.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BillingApi.new

begin
  # Effective limits + current usage for the calling tenant.
  api_instance.get_quota_api
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_quota_api: #{e}"
end
```

#### Using the get_quota_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> get_quota_api_with_http_info

```ruby
begin
  # Effective limits + current usage for the calling tenant.
  data, status_code, headers = api_instance.get_quota_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_quota_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_subscription_api

> <ApiResponseSubscriptionOverview> get_subscription_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BillingApi.new

begin
  
  result = api_instance.get_subscription_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_subscription_api: #{e}"
end
```

#### Using the get_subscription_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseSubscriptionOverview>, Integer, Hash)> get_subscription_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.get_subscription_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseSubscriptionOverview>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_subscription_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiResponseSubscriptionOverview**](ApiResponseSubscriptionOverview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_usage_api

> get_usage_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BillingApi.new
opts = {
  meter: 'meter_example' # String | 
}

begin
  
  api_instance.get_usage_api(opts)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_usage_api: #{e}"
end
```

#### Using the get_usage_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> get_usage_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_usage_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->get_usage_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **meter** | **String** |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## paddle_subscription_webhook

> paddle_subscription_webhook

Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BillingApi.new

begin
  # Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).
  api_instance.paddle_subscription_webhook
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->paddle_subscription_webhook: #{e}"
end
```

#### Using the paddle_subscription_webhook_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> paddle_subscription_webhook_with_http_info

```ruby
begin
  # Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).
  data, status_code, headers = api_instance.paddle_subscription_webhook_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->paddle_subscription_webhook_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## put_quota_api

> put_quota_api(quota_override)

Write the per-tenant quota override (`admin:settings`). An empty object clears the override.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BillingApi.new
quota_override = SimplebillyApi::QuotaOverride.new # QuotaOverride | 

begin
  # Write the per-tenant quota override (`admin:settings`). An empty object clears the override.
  api_instance.put_quota_api(quota_override)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->put_quota_api: #{e}"
end
```

#### Using the put_quota_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> put_quota_api_with_http_info(quota_override)

```ruby
begin
  # Write the per-tenant quota override (`admin:settings`). An empty object clears the override.
  data, status_code, headers = api_instance.put_quota_api_with_http_info(quota_override)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BillingApi->put_quota_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quota_override** | [**QuotaOverride**](QuotaOverride.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

