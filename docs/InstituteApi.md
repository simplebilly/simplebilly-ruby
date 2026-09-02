# SimplebillyApi::InstituteApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**institute_status_api**](InstituteApi.md#institute_status_api) | **GET** /api/v1/bookkeeping/institute/status |  |


## institute_status_api

> <InstituteStatus> institute_status_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InstituteApi.new

begin
  
  result = api_instance.institute_status_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InstituteApi->institute_status_api: #{e}"
end
```

#### Using the institute_status_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InstituteStatus>, Integer, Hash)> institute_status_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.institute_status_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InstituteStatus>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InstituteApi->institute_status_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**InstituteStatus**](InstituteStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

