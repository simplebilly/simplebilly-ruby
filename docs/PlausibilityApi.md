# SimplebillyApi::PlausibilityApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**plausibility_check_api**](PlausibilityApi.md#plausibility_check_api) | **GET** /api/v1/bookkeeping/plausibility |  |


## plausibility_check_api

> <PlausibilityReport> plausibility_check_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PlausibilityApi.new
opts = {
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example' # String | 
}

begin
  
  result = api_instance.plausibility_check_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PlausibilityApi->plausibility_check_api: #{e}"
end
```

#### Using the plausibility_check_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PlausibilityReport>, Integer, Hash)> plausibility_check_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.plausibility_check_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PlausibilityReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PlausibilityApi->plausibility_check_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |

### Return type

[**PlausibilityReport**](PlausibilityReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

