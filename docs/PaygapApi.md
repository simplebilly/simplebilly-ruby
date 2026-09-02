# SimplebillyApi::PaygapApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**paygap_auskunft_api**](PaygapApi.md#paygap_auskunft_api) | **GET** /api/v1/bookkeeping/paygap/auskunft/{employee_id} |  |
| [**paygap_export_api**](PaygapApi.md#paygap_export_api) | **GET** /api/v1/bookkeeping/paygap/export |  |
| [**paygap_report_api**](PaygapApi.md#paygap_report_api) | **GET** /api/v1/bookkeeping/paygap/report |  |


## paygap_auskunft_api

> <PayGapInfoResponse> paygap_auskunft_api(employee_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaygapApi.new
employee_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.paygap_auskunft_api(employee_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaygapApi->paygap_auskunft_api: #{e}"
end
```

#### Using the paygap_auskunft_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayGapInfoResponse>, Integer, Hash)> paygap_auskunft_api_with_http_info(employee_id)

```ruby
begin
  
  data, status_code, headers = api_instance.paygap_auskunft_api_with_http_info(employee_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayGapInfoResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaygapApi->paygap_auskunft_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **employee_id** | **String** |  |  |

### Return type

[**PayGapInfoResponse**](PayGapInfoResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## paygap_export_api

> <PayGapExportResponse> paygap_export_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaygapApi.new

begin
  
  result = api_instance.paygap_export_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaygapApi->paygap_export_api: #{e}"
end
```

#### Using the paygap_export_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayGapExportResponse>, Integer, Hash)> paygap_export_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.paygap_export_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayGapExportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaygapApi->paygap_export_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PayGapExportResponse**](PayGapExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## paygap_report_api

> <PayGapReport> paygap_report_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaygapApi.new

begin
  
  result = api_instance.paygap_report_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaygapApi->paygap_report_api: #{e}"
end
```

#### Using the paygap_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayGapReport>, Integer, Hash)> paygap_report_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.paygap_report_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayGapReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaygapApi->paygap_report_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PayGapReport**](PayGapReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

