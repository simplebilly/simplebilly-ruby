# SimplebillyApi::AutomationsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_automations**](AutomationsApi.md#list_automations) | **GET** /api/v1/automations |  |
| [**trigger_automation**](AutomationsApi.md#trigger_automation) | **POST** /api/v1/automations/{key}/trigger |  |
| [**update_automation**](AutomationsApi.md#update_automation) | **PUT** /api/v1/automations/{key} |  |


## list_automations

> <Array<AutomationDto>> list_automations



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AutomationsApi.new

begin
  
  result = api_instance.list_automations
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AutomationsApi->list_automations: #{e}"
end
```

#### Using the list_automations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AutomationDto>>, Integer, Hash)> list_automations_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_automations_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AutomationDto>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AutomationsApi->list_automations_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;AutomationDto&gt;**](AutomationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## trigger_automation

> Object trigger_automation(key)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AutomationsApi.new
key = 'key_example' # String | 

begin
  
  result = api_instance.trigger_automation(key)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AutomationsApi->trigger_automation: #{e}"
end
```

#### Using the trigger_automation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> trigger_automation_with_http_info(key)

```ruby
begin
  
  data, status_code, headers = api_instance.trigger_automation_with_http_info(key)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AutomationsApi->trigger_automation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_automation

> <AutomationDto> update_automation(key, update_automation)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AutomationsApi.new
key = 'key_example' # String | 
update_automation = SimplebillyApi::UpdateAutomation.new # UpdateAutomation | 

begin
  
  result = api_instance.update_automation(key, update_automation)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AutomationsApi->update_automation: #{e}"
end
```

#### Using the update_automation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AutomationDto>, Integer, Hash)> update_automation_with_http_info(key, update_automation)

```ruby
begin
  
  data, status_code, headers = api_instance.update_automation_with_http_info(key, update_automation)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AutomationDto>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AutomationsApi->update_automation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** |  |  |
| **update_automation** | [**UpdateAutomation**](UpdateAutomation.md) |  |  |

### Return type

[**AutomationDto**](AutomationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

