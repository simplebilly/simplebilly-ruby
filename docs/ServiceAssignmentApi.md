# SimplebillyApi::ServiceAssignmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_service_assignment**](ServiceAssignmentApi.md#create_service_assignment) | **POST** /api/v1/service-assignments |  |
| [**delete_service_assignment**](ServiceAssignmentApi.md#delete_service_assignment) | **DELETE** /api/v1/service-assignments/{id} |  |
| [**get_service_assignment**](ServiceAssignmentApi.md#get_service_assignment) | **GET** /api/v1/service-assignments/{id} |  |
| [**get_service_assignments**](ServiceAssignmentApi.md#get_service_assignments) | **GET** /api/v1/service-assignments/ |  |
| [**update_service_assignment**](ServiceAssignmentApi.md#update_service_assignment) | **PUT** /api/v1/service-assignments/{id} |  |


## create_service_assignment

> <ServiceAssignment> create_service_assignment(service_assignment_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceAssignmentApi.new
service_assignment_create = SimplebillyApi::ServiceAssignmentCreate.new # ServiceAssignmentCreate | 

begin
  
  result = api_instance.create_service_assignment(service_assignment_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->create_service_assignment: #{e}"
end
```

#### Using the create_service_assignment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ServiceAssignment>, Integer, Hash)> create_service_assignment_with_http_info(service_assignment_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_service_assignment_with_http_info(service_assignment_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ServiceAssignment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->create_service_assignment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **service_assignment_create** | [**ServiceAssignmentCreate**](ServiceAssignmentCreate.md) |  |  |

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_service_assignment

> delete_service_assignment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceAssignmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_service_assignment(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->delete_service_assignment: #{e}"
end
```

#### Using the delete_service_assignment_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_service_assignment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_service_assignment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->delete_service_assignment_with_http_info: #{e}"
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
- **Accept**: application/json


## get_service_assignment

> <ServiceAssignment> get_service_assignment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceAssignmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_service_assignment(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->get_service_assignment: #{e}"
end
```

#### Using the get_service_assignment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ServiceAssignment>, Integer, Hash)> get_service_assignment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_service_assignment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ServiceAssignment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->get_service_assignment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_service_assignments

> <Array<ServiceAssignment>> get_service_assignments(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceAssignmentApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_service_assignments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->get_service_assignments: #{e}"
end
```

#### Using the get_service_assignments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ServiceAssignment>>, Integer, Hash)> get_service_assignments_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_service_assignments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ServiceAssignment>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->get_service_assignments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **include_deleted** | **Boolean** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] |

### Return type

[**Array&lt;ServiceAssignment&gt;**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_service_assignment

> <ServiceAssignment> update_service_assignment(id, service_assignment_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceAssignmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
service_assignment_update = SimplebillyApi::ServiceAssignmentUpdate.new # ServiceAssignmentUpdate | 

begin
  
  result = api_instance.update_service_assignment(id, service_assignment_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->update_service_assignment: #{e}"
end
```

#### Using the update_service_assignment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ServiceAssignment>, Integer, Hash)> update_service_assignment_with_http_info(id, service_assignment_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_service_assignment_with_http_info(id, service_assignment_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ServiceAssignment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceAssignmentApi->update_service_assignment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **service_assignment_update** | [**ServiceAssignmentUpdate**](ServiceAssignmentUpdate.md) |  |  |

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

