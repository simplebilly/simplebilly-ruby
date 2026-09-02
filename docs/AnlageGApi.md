# SimplebillyApi::AnlageGApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**anlage_g_api**](AnlageGApi.md#anlage_g_api) | **GET** /api/v1/bookkeeping/anlage-g |  |


## anlage_g_api

> <AnlageGErgebnis> anlage_g_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AnlageGApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.anlage_g_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AnlageGApi->anlage_g_api: #{e}"
end
```

#### Using the anlage_g_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AnlageGErgebnis>, Integer, Hash)> anlage_g_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.anlage_g_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AnlageGErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AnlageGApi->anlage_g_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**AnlageGErgebnis**](AnlageGErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

