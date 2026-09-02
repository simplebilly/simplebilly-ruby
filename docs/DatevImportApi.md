# SimplebillyApi::DatevImportApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**datev_import_api**](DatevImportApi.md#datev_import_api) | **POST** /api/v1/bookkeeping/datev/import |  |


## datev_import_api

> <DatevImportResponse> datev_import_api(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DatevImportApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.datev_import_api(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DatevImportApi->datev_import_api: #{e}"
end
```

#### Using the datev_import_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DatevImportResponse>, Integer, Hash)> datev_import_api_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.datev_import_api_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DatevImportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DatevImportApi->datev_import_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

[**DatevImportResponse**](DatevImportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

