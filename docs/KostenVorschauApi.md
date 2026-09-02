# SimplebillyApi::KostenVorschauApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**kosten_vorschau_api**](KostenVorschauApi.md#kosten_vorschau_api) | **GET** /api/v1/bookkeeping/kosten-vorschau |  |


## kosten_vorschau_api

> <KostenVorschau> kosten_vorschau_api(year, month)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KostenVorschauApi.new
year = 56 # Integer | 
month = 56 # Integer | 

begin
  
  result = api_instance.kosten_vorschau_api(year, month)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KostenVorschauApi->kosten_vorschau_api: #{e}"
end
```

#### Using the kosten_vorschau_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KostenVorschau>, Integer, Hash)> kosten_vorschau_api_with_http_info(year, month)

```ruby
begin
  
  data, status_code, headers = api_instance.kosten_vorschau_api_with_http_info(year, month)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KostenVorschau>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KostenVorschauApi->kosten_vorschau_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |
| **month** | **Integer** |  |  |

### Return type

[**KostenVorschau**](KostenVorschau.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

