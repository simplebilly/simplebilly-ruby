# SimplebillyApi::ServiceJobApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_service_job**](ServiceJobApi.md#create_service_job) | **POST** /api/v1/service-jobs |  |
| [**delete_service_job**](ServiceJobApi.md#delete_service_job) | **DELETE** /api/v1/service-jobs/{id} |  |
| [**get_service_job**](ServiceJobApi.md#get_service_job) | **GET** /api/v1/service-jobs/{id} |  |
| [**get_service_jobs**](ServiceJobApi.md#get_service_jobs) | **GET** /api/v1/service-jobs/ |  |
| [**update_service_job**](ServiceJobApi.md#update_service_job) | **PUT** /api/v1/service-jobs/{id} |  |


## create_service_job

> <ServiceJob> create_service_job(service_job_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceJobApi.new
service_job_create = SimplebillyApi::ServiceJobCreate.new # ServiceJobCreate | 

begin
  
  result = api_instance.create_service_job(service_job_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->create_service_job: #{e}"
end
```

#### Using the create_service_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ServiceJob>, Integer, Hash)> create_service_job_with_http_info(service_job_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_service_job_with_http_info(service_job_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ServiceJob>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->create_service_job_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **service_job_create** | [**ServiceJobCreate**](ServiceJobCreate.md) |  |  |

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_service_job

> delete_service_job(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceJobApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_service_job(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->delete_service_job: #{e}"
end
```

#### Using the delete_service_job_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_service_job_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_service_job_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->delete_service_job_with_http_info: #{e}"
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


## get_service_job

> <ServiceJob> get_service_job(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceJobApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_service_job(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->get_service_job: #{e}"
end
```

#### Using the get_service_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ServiceJob>, Integer, Hash)> get_service_job_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_service_job_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ServiceJob>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->get_service_job_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_service_jobs

> <Array<ServiceJob>> get_service_jobs(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceJobApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_service_jobs(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->get_service_jobs: #{e}"
end
```

#### Using the get_service_jobs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ServiceJob>>, Integer, Hash)> get_service_jobs_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_service_jobs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ServiceJob>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->get_service_jobs_with_http_info: #{e}"
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

[**Array&lt;ServiceJob&gt;**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_service_job

> <ServiceJob> update_service_job(id, service_job_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ServiceJobApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
service_job_update = SimplebillyApi::ServiceJobUpdate.new # ServiceJobUpdate | 

begin
  
  result = api_instance.update_service_job(id, service_job_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->update_service_job: #{e}"
end
```

#### Using the update_service_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ServiceJob>, Integer, Hash)> update_service_job_with_http_info(id, service_job_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_service_job_with_http_info(id, service_job_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ServiceJob>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ServiceJobApi->update_service_job_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **service_job_update** | [**ServiceJobUpdate**](ServiceJobUpdate.md) |  |  |

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

