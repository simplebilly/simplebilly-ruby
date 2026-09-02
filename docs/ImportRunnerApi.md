# SimplebillyApi::ImportRunnerApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_import_status**](ImportRunnerApi.md#get_import_status) | **GET** /api/v1/import/{job_id} |  |
| [**start_import**](ImportRunnerApi.md#start_import) | **POST** /api/v1/import/start |  |
| [**test_import_connection**](ImportRunnerApi.md#test_import_connection) | **POST** /api/v1/import/test |  |


## get_import_status

> <ImportJobStatus> get_import_status(job_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ImportRunnerApi.new
job_id = 'job_id_example' # String | 

begin
  
  result = api_instance.get_import_status(job_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ImportRunnerApi->get_import_status: #{e}"
end
```

#### Using the get_import_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportJobStatus>, Integer, Hash)> get_import_status_with_http_info(job_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_import_status_with_http_info(job_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportJobStatus>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ImportRunnerApi->get_import_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** |  |  |

### Return type

[**ImportJobStatus**](ImportJobStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## start_import

> <ImportStartResponse> start_import(import_start_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ImportRunnerApi.new
import_start_request = SimplebillyApi::ImportStartRequest.new({api_key: 'api_key_example', provider: 'provider_example', years: [37]}) # ImportStartRequest | 

begin
  
  result = api_instance.start_import(import_start_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ImportRunnerApi->start_import: #{e}"
end
```

#### Using the start_import_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportStartResponse>, Integer, Hash)> start_import_with_http_info(import_start_request)

```ruby
begin
  
  data, status_code, headers = api_instance.start_import_with_http_info(import_start_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportStartResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ImportRunnerApi->start_import_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **import_start_request** | [**ImportStartRequest**](ImportStartRequest.md) |  |  |

### Return type

[**ImportStartResponse**](ImportStartResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## test_import_connection

> <ImportTestResponse> test_import_connection(import_test_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ImportRunnerApi.new
import_test_request = SimplebillyApi::ImportTestRequest.new({api_key: 'api_key_example', provider: 'provider_example'}) # ImportTestRequest | 

begin
  
  result = api_instance.test_import_connection(import_test_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ImportRunnerApi->test_import_connection: #{e}"
end
```

#### Using the test_import_connection_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportTestResponse>, Integer, Hash)> test_import_connection_with_http_info(import_test_request)

```ruby
begin
  
  data, status_code, headers = api_instance.test_import_connection_with_http_info(import_test_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportTestResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ImportRunnerApi->test_import_connection_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **import_test_request** | [**ImportTestRequest**](ImportTestRequest.md) |  |  |

### Return type

[**ImportTestResponse**](ImportTestResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

