# SimplebillyApi::ComplianceTrainingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_compliance_training**](ComplianceTrainingApi.md#create_compliance_training) | **POST** /api/v1/compliance-trainings |  |
| [**delete_compliance_training**](ComplianceTrainingApi.md#delete_compliance_training) | **DELETE** /api/v1/compliance-trainings/{id} |  |
| [**get_compliance_training**](ComplianceTrainingApi.md#get_compliance_training) | **GET** /api/v1/compliance-trainings/{id} |  |
| [**get_compliance_trainings**](ComplianceTrainingApi.md#get_compliance_trainings) | **GET** /api/v1/compliance-trainings/ |  |
| [**update_compliance_training**](ComplianceTrainingApi.md#update_compliance_training) | **PUT** /api/v1/compliance-trainings/{id} |  |


## create_compliance_training

> <ComplianceTraining> create_compliance_training(compliance_training_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ComplianceTrainingApi.new
compliance_training_create = SimplebillyApi::ComplianceTrainingCreate.new # ComplianceTrainingCreate | 

begin
  
  result = api_instance.create_compliance_training(compliance_training_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->create_compliance_training: #{e}"
end
```

#### Using the create_compliance_training_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ComplianceTraining>, Integer, Hash)> create_compliance_training_with_http_info(compliance_training_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_compliance_training_with_http_info(compliance_training_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ComplianceTraining>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->create_compliance_training_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **compliance_training_create** | [**ComplianceTrainingCreate**](ComplianceTrainingCreate.md) |  |  |

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_compliance_training

> delete_compliance_training(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ComplianceTrainingApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_compliance_training(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->delete_compliance_training: #{e}"
end
```

#### Using the delete_compliance_training_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_compliance_training_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_compliance_training_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->delete_compliance_training_with_http_info: #{e}"
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


## get_compliance_training

> <ComplianceTraining> get_compliance_training(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ComplianceTrainingApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_compliance_training(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->get_compliance_training: #{e}"
end
```

#### Using the get_compliance_training_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ComplianceTraining>, Integer, Hash)> get_compliance_training_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_compliance_training_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ComplianceTraining>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->get_compliance_training_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_compliance_trainings

> <Array<ComplianceTraining>> get_compliance_trainings(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ComplianceTrainingApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_compliance_trainings(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->get_compliance_trainings: #{e}"
end
```

#### Using the get_compliance_trainings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ComplianceTraining>>, Integer, Hash)> get_compliance_trainings_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_compliance_trainings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ComplianceTraining>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->get_compliance_trainings_with_http_info: #{e}"
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

[**Array&lt;ComplianceTraining&gt;**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_compliance_training

> <ComplianceTraining> update_compliance_training(id, compliance_training_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ComplianceTrainingApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
compliance_training_update = SimplebillyApi::ComplianceTrainingUpdate.new # ComplianceTrainingUpdate | 

begin
  
  result = api_instance.update_compliance_training(id, compliance_training_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->update_compliance_training: #{e}"
end
```

#### Using the update_compliance_training_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ComplianceTraining>, Integer, Hash)> update_compliance_training_with_http_info(id, compliance_training_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_compliance_training_with_http_info(id, compliance_training_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ComplianceTraining>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ComplianceTrainingApi->update_compliance_training_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **compliance_training_update** | [**ComplianceTrainingUpdate**](ComplianceTrainingUpdate.md) |  |  |

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

