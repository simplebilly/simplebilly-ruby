# SimplebillyApi::EventSubscriptionApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_event_subscription**](EventSubscriptionApi.md#create_event_subscription) | **POST** /api/v1/event-subscriptions |  |
| [**delete_event_subscription**](EventSubscriptionApi.md#delete_event_subscription) | **DELETE** /api/v1/event-subscriptions/{subscription_id} |  |
| [**list_event_subscriptions**](EventSubscriptionApi.md#list_event_subscriptions) | **GET** /api/v1/event-subscriptions/ |  |


## create_event_subscription

> <EventSubscription> create_event_subscription(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EventSubscriptionApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.create_event_subscription(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EventSubscriptionApi->create_event_subscription: #{e}"
end
```

#### Using the create_event_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EventSubscription>, Integer, Hash)> create_event_subscription_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.create_event_subscription_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EventSubscription>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EventSubscriptionApi->create_event_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

[**EventSubscription**](EventSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_event_subscription

> delete_event_subscription(subscription_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EventSubscriptionApi.new
subscription_id = 'subscription_id_example' # String | 

begin
  
  api_instance.delete_event_subscription(subscription_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EventSubscriptionApi->delete_event_subscription: #{e}"
end
```

#### Using the delete_event_subscription_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_event_subscription_with_http_info(subscription_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_event_subscription_with_http_info(subscription_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EventSubscriptionApi->delete_event_subscription_with_http_info: #{e}"
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
- **Accept**: application/json


## list_event_subscriptions

> <Array<EventSubscription>> list_event_subscriptions



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EventSubscriptionApi.new

begin
  
  result = api_instance.list_event_subscriptions
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EventSubscriptionApi->list_event_subscriptions: #{e}"
end
```

#### Using the list_event_subscriptions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<EventSubscription>>, Integer, Hash)> list_event_subscriptions_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_event_subscriptions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<EventSubscription>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EventSubscriptionApi->list_event_subscriptions_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;EventSubscription&gt;**](EventSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

