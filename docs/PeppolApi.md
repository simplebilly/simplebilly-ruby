# SimplebillyApi::PeppolApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**peppol_api**](PeppolApi.md#peppol_api) | **GET** /api/v1/invoices/{id}/peppol |  |


## peppol_api

> <PeppolResponse> peppol_api(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PeppolApi.new
id = 'id_example' # String | 

begin
  
  result = api_instance.peppol_api(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PeppolApi->peppol_api: #{e}"
end
```

#### Using the peppol_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PeppolResponse>, Integer, Hash)> peppol_api_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.peppol_api_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PeppolResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PeppolApi->peppol_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**PeppolResponse**](PeppolResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

