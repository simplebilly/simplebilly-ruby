# SimplebillyApi::KonzernApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**konzern_export_api**](KonzernApi.md#konzern_export_api) | **GET** /api/v1/bookkeeping/konzern/status/export |  |
| [**konzern_status_api**](KonzernApi.md#konzern_status_api) | **GET** /api/v1/bookkeeping/konzern/status |  |


## konzern_export_api

> <KonzernExportResponse> konzern_export_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KonzernApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.konzern_export_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KonzernApi->konzern_export_api: #{e}"
end
```

#### Using the konzern_export_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KonzernExportResponse>, Integer, Hash)> konzern_export_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.konzern_export_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KonzernExportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KonzernApi->konzern_export_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**KonzernExportResponse**](KonzernExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## konzern_status_api

> <KonzernStatus> konzern_status_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KonzernApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.konzern_status_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KonzernApi->konzern_status_api: #{e}"
end
```

#### Using the konzern_status_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KonzernStatus>, Integer, Hash)> konzern_status_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.konzern_status_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KonzernStatus>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KonzernApi->konzern_status_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**KonzernStatus**](KonzernStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

