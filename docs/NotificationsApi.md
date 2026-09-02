# SimplebillyApi::NotificationsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_notification**](NotificationsApi.md#delete_notification) | **DELETE** /api/v1/notifications/{id} |  |
| [**list_notifications**](NotificationsApi.md#list_notifications) | **GET** /api/v1/notifications |  |
| [**mark_all_read**](NotificationsApi.md#mark_all_read) | **PUT** /api/v1/notifications/read-all |  |
| [**mark_as_read**](NotificationsApi.md#mark_as_read) | **PUT** /api/v1/notifications/{id}/read |  |
| [**unread_count**](NotificationsApi.md#unread_count) | **GET** /api/v1/notifications/unread-count |  |


## delete_notification

> delete_notification(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::NotificationsApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_notification(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->delete_notification: #{e}"
end
```

#### Using the delete_notification_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_notification_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_notification_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->delete_notification_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_notifications

> <Array<NotificationDto>> list_notifications



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::NotificationsApi.new

begin
  
  result = api_instance.list_notifications
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->list_notifications: #{e}"
end
```

#### Using the list_notifications_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<NotificationDto>>, Integer, Hash)> list_notifications_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_notifications_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<NotificationDto>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->list_notifications_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;NotificationDto&gt;**](NotificationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## mark_all_read

> Integer mark_all_read



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::NotificationsApi.new

begin
  
  result = api_instance.mark_all_read
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->mark_all_read: #{e}"
end
```

#### Using the mark_all_read_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Integer, Integer, Hash)> mark_all_read_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.mark_all_read_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Integer
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->mark_all_read_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Integer**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain


## mark_as_read

> mark_as_read(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::NotificationsApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.mark_as_read(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->mark_as_read: #{e}"
end
```

#### Using the mark_as_read_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> mark_as_read_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.mark_as_read_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->mark_as_read_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## unread_count

> Integer unread_count



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::NotificationsApi.new

begin
  
  result = api_instance.unread_count
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->unread_count: #{e}"
end
```

#### Using the unread_count_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Integer, Integer, Hash)> unread_count_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.unread_count_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Integer
rescue SimplebillyApi::ApiError => e
  puts "Error when calling NotificationsApi->unread_count_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Integer**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain

