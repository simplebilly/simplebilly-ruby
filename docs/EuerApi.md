# SimplebillyApi::EuerApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**euer_api**](EuerApi.md#euer_api) | **GET** /api/v1/bookkeeping/euer |  |
| [**euer_kategorien_api**](EuerApi.md#euer_kategorien_api) | **GET** /api/v1/bookkeeping/euer/kategorien |  |


## euer_api

> <EuerErgebnis> euer_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EuerApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.euer_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EuerApi->euer_api: #{e}"
end
```

#### Using the euer_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EuerErgebnis>, Integer, Hash)> euer_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.euer_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EuerErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EuerApi->euer_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**EuerErgebnis**](EuerErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## euer_kategorien_api

> <EuerDetailErgebnis> euer_kategorien_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EuerApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.euer_kategorien_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EuerApi->euer_kategorien_api: #{e}"
end
```

#### Using the euer_kategorien_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EuerDetailErgebnis>, Integer, Hash)> euer_kategorien_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.euer_kategorien_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EuerDetailErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EuerApi->euer_kategorien_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**EuerDetailErgebnis**](EuerDetailErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

