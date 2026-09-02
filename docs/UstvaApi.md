# SimplebillyApi::UstvaApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**jahresust_api**](UstvaApi.md#jahresust_api) | **GET** /api/v1/bookkeeping/jahresust |  |
| [**ustva_api**](UstvaApi.md#ustva_api) | **GET** /api/v1/bookkeeping/ustva |  |


## jahresust_api

> <JahresUstErgebnis> jahresust_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UstvaApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.jahresust_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UstvaApi->jahresust_api: #{e}"
end
```

#### Using the jahresust_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JahresUstErgebnis>, Integer, Hash)> jahresust_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.jahresust_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JahresUstErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UstvaApi->jahresust_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**JahresUstErgebnis**](JahresUstErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## ustva_api

> <UstvaErgebnis> ustva_api(zeitraum)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UstvaApi.new
zeitraum = 'zeitraum_example' # String | 

begin
  
  result = api_instance.ustva_api(zeitraum)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UstvaApi->ustva_api: #{e}"
end
```

#### Using the ustva_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UstvaErgebnis>, Integer, Hash)> ustva_api_with_http_info(zeitraum)

```ruby
begin
  
  data, status_code, headers = api_instance.ustva_api_with_http_info(zeitraum)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UstvaErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UstvaApi->ustva_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **zeitraum** | **String** |  |  |

### Return type

[**UstvaErgebnis**](UstvaErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

