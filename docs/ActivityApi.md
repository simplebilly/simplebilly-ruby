# SimplebillyApi::ActivityApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_activity**](ActivityApi.md#create_activity) | **POST** /api/v1/activities |  |
| [**delete_activity**](ActivityApi.md#delete_activity) | **DELETE** /api/v1/activities/{activity_id} |  |
| [**get_activity**](ActivityApi.md#get_activity) | **GET** /api/v1/activities/{activity_id} |  |
| [**list_activities**](ActivityApi.md#list_activities) | **GET** /api/v1/activities/ |  |
| [**update_activity**](ActivityApi.md#update_activity) | **PUT** /api/v1/activities/{activity_id} |  |
| [**update_activity_status**](ActivityApi.md#update_activity_status) | **PUT** /api/v1/activities/{activity_id}/status |  |


## create_activity

> <Activity> create_activity(activity)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ActivityApi.new
activity = SimplebillyApi::Activity.new({activity_type: SimplebillyApi::ActivityType::CALL, status: SimplebillyApi::ActivityStatus::OPEN, subject: 'subject_example'}) # Activity | 

begin
  
  result = api_instance.create_activity(activity)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->create_activity: #{e}"
end
```

#### Using the create_activity_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Activity>, Integer, Hash)> create_activity_with_http_info(activity)

```ruby
begin
  
  data, status_code, headers = api_instance.create_activity_with_http_info(activity)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Activity>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->create_activity_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity** | [**Activity**](Activity.md) |  |  |

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_activity

> delete_activity(activity_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ActivityApi.new
activity_id = 'activity_id_example' # String | 

begin
  
  api_instance.delete_activity(activity_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->delete_activity: #{e}"
end
```

#### Using the delete_activity_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_activity_with_http_info(activity_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_activity_with_http_info(activity_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->delete_activity_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_activity

> <Activity> get_activity(activity_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ActivityApi.new
activity_id = 'activity_id_example' # String | 

begin
  
  result = api_instance.get_activity(activity_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->get_activity: #{e}"
end
```

#### Using the get_activity_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Activity>, Integer, Hash)> get_activity_with_http_info(activity_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_activity_with_http_info(activity_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Activity>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->get_activity_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_id** | **String** |  |  |

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_activities

> <Array<Activity>> list_activities(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ActivityApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  contact_id: 'contact_id_example', # String | 
  activity_type: 'activity_type_example', # String | 
  status: 'status_example', # String | 
  assigned_to: 'assigned_to_example', # String | 
  overdue_only: true # Boolean | Only show overdue follow-ups.
}

begin
  
  result = api_instance.list_activities(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->list_activities: #{e}"
end
```

#### Using the list_activities_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Activity>>, Integer, Hash)> list_activities_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_activities_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Activity>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->list_activities_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **contact_id** | **String** |  | [optional] |
| **activity_type** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **assigned_to** | **String** |  | [optional] |
| **overdue_only** | **Boolean** | Only show overdue follow-ups. | [optional] |

### Return type

[**Array&lt;Activity&gt;**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_activity

> <Activity> update_activity(activity_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ActivityApi.new
activity_id = 'activity_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_activity(activity_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->update_activity: #{e}"
end
```

#### Using the update_activity_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Activity>, Integer, Hash)> update_activity_with_http_info(activity_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_activity_with_http_info(activity_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Activity>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->update_activity_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_activity_status

> <Activity> update_activity_status(activity_id, activity_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ActivityApi.new
activity_id = 'activity_id_example' # String | 
activity_status_update = SimplebillyApi::ActivityStatusUpdate.new({status: 'status_example'}) # ActivityStatusUpdate | 

begin
  
  result = api_instance.update_activity_status(activity_id, activity_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->update_activity_status: #{e}"
end
```

#### Using the update_activity_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Activity>, Integer, Hash)> update_activity_status_with_http_info(activity_id, activity_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_activity_status_with_http_info(activity_id, activity_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Activity>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ActivityApi->update_activity_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_id** | **String** |  |  |
| **activity_status_update** | [**ActivityStatusUpdate**](ActivityStatusUpdate.md) |  |  |

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

