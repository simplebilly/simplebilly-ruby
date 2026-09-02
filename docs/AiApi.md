# SimplebillyApi::AiApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**ai_suggest_api**](AiApi.md#ai_suggest_api) | **POST** /api/v1/support/ai/suggest |  |
| [**create_worker_api**](AiApi.md#create_worker_api) | **POST** /api/v1/support/ai/workers |  |
| [**list_workers_api**](AiApi.md#list_workers_api) | **GET** /api/v1/support/ai/workers |  |
| [**run_worker_api**](AiApi.md#run_worker_api) | **POST** /api/v1/support/ai/workers/{worker_id}/run |  |


## ai_suggest_api

> <AiSuggestion> ai_suggest_api(ai_suggestion_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AiApi.new
ai_suggestion_request = SimplebillyApi::AiSuggestionRequest.new({ticket_id: 'ticket_id_example'}) # AiSuggestionRequest | 

begin
  
  result = api_instance.ai_suggest_api(ai_suggestion_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->ai_suggest_api: #{e}"
end
```

#### Using the ai_suggest_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AiSuggestion>, Integer, Hash)> ai_suggest_api_with_http_info(ai_suggestion_request)

```ruby
begin
  
  data, status_code, headers = api_instance.ai_suggest_api_with_http_info(ai_suggestion_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AiSuggestion>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->ai_suggest_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ai_suggestion_request** | [**AiSuggestionRequest**](AiSuggestionRequest.md) |  |  |

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_worker_api

> <AiWorkerConfig> create_worker_api(ai_config_dto)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AiApi.new
ai_config_dto = SimplebillyApi::AiConfigDto.new({model: 'model_example', name: 'name_example', provider: 'provider_example'}) # AiConfigDto | 

begin
  
  result = api_instance.create_worker_api(ai_config_dto)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->create_worker_api: #{e}"
end
```

#### Using the create_worker_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AiWorkerConfig>, Integer, Hash)> create_worker_api_with_http_info(ai_config_dto)

```ruby
begin
  
  data, status_code, headers = api_instance.create_worker_api_with_http_info(ai_config_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AiWorkerConfig>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->create_worker_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ai_config_dto** | [**AiConfigDto**](AiConfigDto.md) |  |  |

### Return type

[**AiWorkerConfig**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_workers_api

> <Array<AiWorkerConfig>> list_workers_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AiApi.new

begin
  
  result = api_instance.list_workers_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->list_workers_api: #{e}"
end
```

#### Using the list_workers_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AiWorkerConfig>>, Integer, Hash)> list_workers_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_workers_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AiWorkerConfig>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->list_workers_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;AiWorkerConfig&gt;**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## run_worker_api

> <AiSuggestion> run_worker_api(worker_id, ai_suggestion_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AiApi.new
worker_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
ai_suggestion_request = SimplebillyApi::AiSuggestionRequest.new({ticket_id: 'ticket_id_example'}) # AiSuggestionRequest | 

begin
  
  result = api_instance.run_worker_api(worker_id, ai_suggestion_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->run_worker_api: #{e}"
end
```

#### Using the run_worker_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AiSuggestion>, Integer, Hash)> run_worker_api_with_http_info(worker_id, ai_suggestion_request)

```ruby
begin
  
  data, status_code, headers = api_instance.run_worker_api_with_http_info(worker_id, ai_suggestion_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AiSuggestion>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AiApi->run_worker_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **worker_id** | **String** |  |  |
| **ai_suggestion_request** | [**AiSuggestionRequest**](AiSuggestionRequest.md) |  |  |

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

