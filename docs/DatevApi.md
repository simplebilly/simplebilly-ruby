# SimplebillyApi::DatevApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**datev_export_api**](DatevApi.md#datev_export_api) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV |
| [**datev_preview_api**](DatevApi.md#datev_preview_api) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review |


## datev_export_api

> <DatevExportResponse> datev_export_api(opts)

Export bookkeeping data as DATEV CSV

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DatevApi.new
opts = {
  account_schema: 'account_schema_example', # String | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # Export bookkeeping data as DATEV CSV
  result = api_instance.datev_export_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DatevApi->datev_export_api: #{e}"
end
```

#### Using the datev_export_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DatevExportResponse>, Integer, Hash)> datev_export_api_with_http_info(opts)

```ruby
begin
  # Export bookkeeping data as DATEV CSV
  data, status_code, headers = api_instance.datev_export_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DatevExportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DatevApi->datev_export_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_schema** | **String** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**DatevExportResponse**](DatevExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## datev_preview_api

> <Array<DatevBookingPreview>> datev_preview_api(opts)

Exported_datev_bookings: returns formed bookings for review

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DatevApi.new
opts = {
  account_schema: 'account_schema_example', # String | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # Exported_datev_bookings: returns formed bookings for review
  result = api_instance.datev_preview_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DatevApi->datev_preview_api: #{e}"
end
```

#### Using the datev_preview_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<DatevBookingPreview>>, Integer, Hash)> datev_preview_api_with_http_info(opts)

```ruby
begin
  # Exported_datev_bookings: returns formed bookings for review
  data, status_code, headers = api_instance.datev_preview_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<DatevBookingPreview>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DatevApi->datev_preview_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_schema** | **String** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**Array&lt;DatevBookingPreview&gt;**](DatevBookingPreview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

