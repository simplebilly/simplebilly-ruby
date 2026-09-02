# SimplebillyApi::StilleApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**stille_export_api**](StilleApi.md#stille_export_api) | **GET** /api/v1/bookkeeping/stille/export |  |
| [**stille_report_api**](StilleApi.md#stille_report_api) | **GET** /api/v1/bookkeeping/stille/report |  |


## stille_export_api

> <StilleExportResponse> stille_export_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StilleApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.stille_export_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StilleApi->stille_export_api: #{e}"
end
```

#### Using the stille_export_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StilleExportResponse>, Integer, Hash)> stille_export_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.stille_export_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StilleExportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StilleApi->stille_export_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**StilleExportResponse**](StilleExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## stille_report_api

> <StilleReport> stille_report_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StilleApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.stille_report_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StilleApi->stille_report_api: #{e}"
end
```

#### Using the stille_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StilleReport>, Integer, Hash)> stille_report_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.stille_report_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StilleReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StilleApi->stille_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**StilleReport**](StilleReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

