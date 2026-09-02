# SimplebillyApi::TrainingAssignmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_training_assignment**](TrainingAssignmentApi.md#create_training_assignment) | **POST** /api/v1/training-assignments |  |
| [**delete_training_assignment**](TrainingAssignmentApi.md#delete_training_assignment) | **DELETE** /api/v1/training-assignments/{id} |  |
| [**get_training_assignment**](TrainingAssignmentApi.md#get_training_assignment) | **GET** /api/v1/training-assignments/{id} |  |
| [**get_training_assignments**](TrainingAssignmentApi.md#get_training_assignments) | **GET** /api/v1/training-assignments/ |  |
| [**update_training_assignment**](TrainingAssignmentApi.md#update_training_assignment) | **PUT** /api/v1/training-assignments/{id} |  |


## create_training_assignment

> <TrainingAssignment> create_training_assignment(training_assignment_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingAssignmentApi.new
training_assignment_create = SimplebillyApi::TrainingAssignmentCreate.new # TrainingAssignmentCreate | 

begin
  
  result = api_instance.create_training_assignment(training_assignment_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->create_training_assignment: #{e}"
end
```

#### Using the create_training_assignment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TrainingAssignment>, Integer, Hash)> create_training_assignment_with_http_info(training_assignment_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_training_assignment_with_http_info(training_assignment_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TrainingAssignment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->create_training_assignment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **training_assignment_create** | [**TrainingAssignmentCreate**](TrainingAssignmentCreate.md) |  |  |

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_training_assignment

> delete_training_assignment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingAssignmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_training_assignment(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->delete_training_assignment: #{e}"
end
```

#### Using the delete_training_assignment_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_training_assignment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_training_assignment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->delete_training_assignment_with_http_info: #{e}"
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


## get_training_assignment

> <TrainingAssignment> get_training_assignment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingAssignmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_training_assignment(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->get_training_assignment: #{e}"
end
```

#### Using the get_training_assignment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TrainingAssignment>, Integer, Hash)> get_training_assignment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_training_assignment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TrainingAssignment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->get_training_assignment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_training_assignments

> <Array<TrainingAssignment>> get_training_assignments(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingAssignmentApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_training_assignments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->get_training_assignments: #{e}"
end
```

#### Using the get_training_assignments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<TrainingAssignment>>, Integer, Hash)> get_training_assignments_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_training_assignments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<TrainingAssignment>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->get_training_assignments_with_http_info: #{e}"
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

[**Array&lt;TrainingAssignment&gt;**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_training_assignment

> <TrainingAssignment> update_training_assignment(id, training_assignment_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingAssignmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
training_assignment_update = SimplebillyApi::TrainingAssignmentUpdate.new # TrainingAssignmentUpdate | 

begin
  
  result = api_instance.update_training_assignment(id, training_assignment_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->update_training_assignment: #{e}"
end
```

#### Using the update_training_assignment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TrainingAssignment>, Integer, Hash)> update_training_assignment_with_http_info(id, training_assignment_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_training_assignment_with_http_info(id, training_assignment_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TrainingAssignment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingAssignmentApi->update_training_assignment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **training_assignment_update** | [**TrainingAssignmentUpdate**](TrainingAssignmentUpdate.md) |  |  |

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

