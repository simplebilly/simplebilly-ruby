# SimplebillyApi::GewinnverwendungApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**gewinnverwendung_api**](GewinnverwendungApi.md#gewinnverwendung_api) | **GET** /api/v1/bookkeeping/gewinnverwendung |  |
| [**gewinnverwendung_export_api**](GewinnverwendungApi.md#gewinnverwendung_export_api) | **GET** /api/v1/bookkeeping/gewinnverwendung/export |  |


## gewinnverwendung_api

> <GewinnverwendungsReport> gewinnverwendung_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GewinnverwendungApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.gewinnverwendung_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GewinnverwendungApi->gewinnverwendung_api: #{e}"
end
```

#### Using the gewinnverwendung_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GewinnverwendungsReport>, Integer, Hash)> gewinnverwendung_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.gewinnverwendung_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GewinnverwendungsReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GewinnverwendungApi->gewinnverwendung_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**GewinnverwendungsReport**](GewinnverwendungsReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gewinnverwendung_export_api

> <GewinnverwendungsExportResponse> gewinnverwendung_export_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GewinnverwendungApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.gewinnverwendung_export_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GewinnverwendungApi->gewinnverwendung_export_api: #{e}"
end
```

#### Using the gewinnverwendung_export_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GewinnverwendungsExportResponse>, Integer, Hash)> gewinnverwendung_export_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.gewinnverwendung_export_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GewinnverwendungsExportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GewinnverwendungApi->gewinnverwendung_export_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**GewinnverwendungsExportResponse**](GewinnverwendungsExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

