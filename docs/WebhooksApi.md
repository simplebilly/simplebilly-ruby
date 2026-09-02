# SimplebillyApi::WebhooksApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_subscription**](WebhooksApi.md#create_subscription) | **POST** /api/v1/webhook-subscriptions | Create a webhook subscription (outbound hook). |
| [**delete_subscription**](WebhooksApi.md#delete_subscription) | **DELETE** /api/v1/webhook-subscriptions/{subscription_id} | Delete a webhook subscription. |
| [**emit_api**](WebhooksApi.md#emit_api) | **POST** /api/v1/webhooks/emit | Manually fire an event against matching hooks (for testing/flows). |
| [**list_event**](WebhooksApi.md#list_event) | **GET** /api/v1/webhook-events | List webhook events (inbound + outbound log). |
| [**list_subscriptions**](WebhooksApi.md#list_subscriptions) | **GET** /api/v1/webhook-subscriptions | List webhook subscriptions for the tenant. |
| [**update_subscription**](WebhooksApi.md#update_subscription) | **PUT** /api/v1/webhook-subscriptions/{subscription_id} | Update a webhook subscription. |


## create_subscription

> <WebhookSubscription> create_subscription(create_subscription_request)

Create a webhook subscription (outbound hook).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WebhooksApi.new
create_subscription_request = SimplebillyApi::CreateSubscriptionRequest.new({event_type: 'event_type_example', name: 'name_example', url: 'url_example'}) # CreateSubscriptionRequest | 

begin
  # Create a webhook subscription (outbound hook).
  result = api_instance.create_subscription(create_subscription_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->create_subscription: #{e}"
end
```

#### Using the create_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookSubscription>, Integer, Hash)> create_subscription_with_http_info(create_subscription_request)

```ruby
begin
  # Create a webhook subscription (outbound hook).
  data, status_code, headers = api_instance.create_subscription_with_http_info(create_subscription_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookSubscription>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->create_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_subscription_request** | [**CreateSubscriptionRequest**](CreateSubscriptionRequest.md) |  |  |

### Return type

[**WebhookSubscription**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_subscription

> delete_subscription(subscription_id)

Delete a webhook subscription.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WebhooksApi.new
subscription_id = 'subscription_id_example' # String | 

begin
  # Delete a webhook subscription.
  api_instance.delete_subscription(subscription_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->delete_subscription: #{e}"
end
```

#### Using the delete_subscription_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_subscription_with_http_info(subscription_id)

```ruby
begin
  # Delete a webhook subscription.
  data, status_code, headers = api_instance.delete_subscription_with_http_info(subscription_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->delete_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## emit_api

> emit_api(emit_event_request)

Manually fire an event against matching hooks (for testing/flows).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WebhooksApi.new
emit_event_request = SimplebillyApi::EmitEventRequest.new({event_type: 'event_type_example'}) # EmitEventRequest | 

begin
  # Manually fire an event against matching hooks (for testing/flows).
  api_instance.emit_api(emit_event_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->emit_api: #{e}"
end
```

#### Using the emit_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> emit_api_with_http_info(emit_event_request)

```ruby
begin
  # Manually fire an event against matching hooks (for testing/flows).
  data, status_code, headers = api_instance.emit_api_with_http_info(emit_event_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->emit_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **emit_event_request** | [**EmitEventRequest**](EmitEventRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## list_event

> <Array<WebhookEvent>> list_event

List webhook events (inbound + outbound log).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WebhooksApi.new

begin
  # List webhook events (inbound + outbound log).
  result = api_instance.list_event
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->list_event: #{e}"
end
```

#### Using the list_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<WebhookEvent>>, Integer, Hash)> list_event_with_http_info

```ruby
begin
  # List webhook events (inbound + outbound log).
  data, status_code, headers = api_instance.list_event_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<WebhookEvent>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->list_event_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;WebhookEvent&gt;**](WebhookEvent.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_subscriptions

> <Array<WebhookSubscription>> list_subscriptions

List webhook subscriptions for the tenant.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WebhooksApi.new

begin
  # List webhook subscriptions for the tenant.
  result = api_instance.list_subscriptions
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->list_subscriptions: #{e}"
end
```

#### Using the list_subscriptions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<WebhookSubscription>>, Integer, Hash)> list_subscriptions_with_http_info

```ruby
begin
  # List webhook subscriptions for the tenant.
  data, status_code, headers = api_instance.list_subscriptions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<WebhookSubscription>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->list_subscriptions_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;WebhookSubscription&gt;**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_subscription

> <WebhookSubscription> update_subscription(subscription_id, update_subscription_request)

Update a webhook subscription.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WebhooksApi.new
subscription_id = 'subscription_id_example' # String | 
update_subscription_request = SimplebillyApi::UpdateSubscriptionRequest.new # UpdateSubscriptionRequest | 

begin
  # Update a webhook subscription.
  result = api_instance.update_subscription(subscription_id, update_subscription_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->update_subscription: #{e}"
end
```

#### Using the update_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookSubscription>, Integer, Hash)> update_subscription_with_http_info(subscription_id, update_subscription_request)

```ruby
begin
  # Update a webhook subscription.
  data, status_code, headers = api_instance.update_subscription_with_http_info(subscription_id, update_subscription_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookSubscription>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WebhooksApi->update_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_id** | **String** |  |  |
| **update_subscription_request** | [**UpdateSubscriptionRequest**](UpdateSubscriptionRequest.md) |  |  |

### Return type

[**WebhookSubscription**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

