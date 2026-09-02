# SimplebillyApi::KstApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**kst_api**](KstApi.md#kst_api) | **GET** /api/v1/bookkeeping/kst |  |


## kst_api

> <KstErgebnis> kst_api(year, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KstApi.new
year = 56 # Integer | 
opts = {
  gewinn: 'gewinn_example' # String | 
}

begin
  
  result = api_instance.kst_api(year, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KstApi->kst_api: #{e}"
end
```

#### Using the kst_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KstErgebnis>, Integer, Hash)> kst_api_with_http_info(year, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.kst_api_with_http_info(year, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KstErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KstApi->kst_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |
| **gewinn** | **String** |  | [optional] |

### Return type

[**KstErgebnis**](KstErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

