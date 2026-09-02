# SimplebillyApi::OssReportApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**oss_report_api**](OssReportApi.md#oss_report_api) | **GET** /api/v1/bookkeeping/oss |  |


## oss_report_api

> <OssReport> oss_report_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OssReportApi.new

begin
  
  result = api_instance.oss_report_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OssReportApi->oss_report_api: #{e}"
end
```

#### Using the oss_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OssReport>, Integer, Hash)> oss_report_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.oss_report_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OssReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OssReportApi->oss_report_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**OssReport**](OssReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

