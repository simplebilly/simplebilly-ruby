# SimplebillyApi::EbilanzApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**ebilanz_report_api**](EbilanzApi.md#ebilanz_report_api) | **GET** /api/v1/bookkeeping/ebilanz |  |
| [**ebilanz_xbrl_export_api**](EbilanzApi.md#ebilanz_xbrl_export_api) | **GET** /api/v1/bookkeeping/ebilanz/xbrl |  |


## ebilanz_report_api

> <EBilanzReport> ebilanz_report_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EbilanzApi.new
opts = {
  year: 56, # Integer | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example' # String | 
}

begin
  
  result = api_instance.ebilanz_report_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EbilanzApi->ebilanz_report_api: #{e}"
end
```

#### Using the ebilanz_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EBilanzReport>, Integer, Hash)> ebilanz_report_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.ebilanz_report_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EBilanzReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EbilanzApi->ebilanz_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |

### Return type

[**EBilanzReport**](EBilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ebilanz_xbrl_export_api

> ebilanz_xbrl_export_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EbilanzApi.new
opts = {
  year: 56, # Integer | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example' # String | 
}

begin
  
  api_instance.ebilanz_xbrl_export_api(opts)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EbilanzApi->ebilanz_xbrl_export_api: #{e}"
end
```

#### Using the ebilanz_xbrl_export_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> ebilanz_xbrl_export_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.ebilanz_xbrl_export_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EbilanzApi->ebilanz_xbrl_export_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml

