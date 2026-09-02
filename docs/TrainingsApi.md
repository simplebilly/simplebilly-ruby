# SimplebillyApi::TrainingsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_my_trainings**](TrainingsApi.md#get_my_trainings) | **GET** /api/v1/trainings/me |  |
| [**get_training_content**](TrainingsApi.md#get_training_content) | **GET** /api/v1/trainings/content/{code} |  |
| [**get_training_overview**](TrainingsApi.md#get_training_overview) | **GET** /api/v1/trainings/overview |  |
| [**submit_training_result**](TrainingsApi.md#submit_training_result) | **POST** /api/v1/trainings/submit-result |  |


## get_my_trainings

> <Array<MyTrainingItem>> get_my_trainings



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingsApi.new

begin
  
  result = api_instance.get_my_trainings
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->get_my_trainings: #{e}"
end
```

#### Using the get_my_trainings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<MyTrainingItem>>, Integer, Hash)> get_my_trainings_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.get_my_trainings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<MyTrainingItem>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->get_my_trainings_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;MyTrainingItem&gt;**](MyTrainingItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_training_content

> <TrainingContent> get_training_content(code)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingsApi.new
code = 'code_example' # String | Training code, e.g. data_privacy

begin
  
  result = api_instance.get_training_content(code)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->get_training_content: #{e}"
end
```

#### Using the get_training_content_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TrainingContent>, Integer, Hash)> get_training_content_with_http_info(code)

```ruby
begin
  
  data, status_code, headers = api_instance.get_training_content_with_http_info(code)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TrainingContent>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->get_training_content_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Training code, e.g. data_privacy |  |

### Return type

[**TrainingContent**](TrainingContent.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_training_overview

> <Array<HrTrainingOverview>> get_training_overview



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingsApi.new

begin
  
  result = api_instance.get_training_overview
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->get_training_overview: #{e}"
end
```

#### Using the get_training_overview_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<HrTrainingOverview>>, Integer, Hash)> get_training_overview_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.get_training_overview_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<HrTrainingOverview>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->get_training_overview_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;HrTrainingOverview&gt;**](HrTrainingOverview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## submit_training_result

> <SubmitResultResponse> submit_training_result(submit_result_dto)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TrainingsApi.new
submit_result_dto = SimplebillyApi::SubmitResultDto.new({answers: [37], score: 37, training_code: 'training_code_example'}) # SubmitResultDto | 

begin
  
  result = api_instance.submit_training_result(submit_result_dto)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->submit_training_result: #{e}"
end
```

#### Using the submit_training_result_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubmitResultResponse>, Integer, Hash)> submit_training_result_with_http_info(submit_result_dto)

```ruby
begin
  
  data, status_code, headers = api_instance.submit_training_result_with_http_info(submit_result_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubmitResultResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TrainingsApi->submit_training_result_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **submit_result_dto** | [**SubmitResultDto**](SubmitResultDto.md) |  |  |

### Return type

[**SubmitResultResponse**](SubmitResultResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

