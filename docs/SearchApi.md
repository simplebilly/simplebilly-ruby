# SimplebillyApi::SearchApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**global_search**](SearchApi.md#global_search) | **GET** /api/v1/search | GET /api/v1/search?q&#x3D;... |
| [**my_permissions**](SearchApi.md#my_permissions) | **GET** /api/v1/me/permissions | GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation. |


## global_search

> Object global_search(q)

GET /api/v1/search?q=...

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SearchApi.new
q = 'q_example' # String | Search text (min 2 chars)

begin
  # GET /api/v1/search?q=...
  result = api_instance.global_search(q)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SearchApi->global_search: #{e}"
end
```

#### Using the global_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> global_search_with_http_info(q)

```ruby
begin
  # GET /api/v1/search?q=...
  data, status_code, headers = api_instance.global_search_with_http_info(q)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SearchApi->global_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search text (min 2 chars) |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## my_permissions

> Object my_permissions

GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SearchApi.new

begin
  # GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.
  result = api_instance.my_permissions
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SearchApi->my_permissions: #{e}"
end
```

#### Using the my_permissions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> my_permissions_with_http_info

```ruby
begin
  # GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.
  data, status_code, headers = api_instance.my_permissions_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SearchApi->my_permissions_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

