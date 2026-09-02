# SimplebillyApi::FristenApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**fristen_api**](FristenApi.md#fristen_api) | **GET** /api/v1/bookkeeping/fristen |  |


## fristen_api

> <FristenErgebnis> fristen_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::FristenApi.new
opts = {
  bundesland: 'bundesland_example', # String | 
  voranmeldungsrhythmus: 'voranmeldungsrhythmus_example', # String | 
  dauerfristverlaengerung: true, # Boolean | 
  est_aktiv: true, # Boolean | 
  gewst_aktiv: true, # Boolean | 
  monate: 56 # Integer | 
}

begin
  
  result = api_instance.fristen_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling FristenApi->fristen_api: #{e}"
end
```

#### Using the fristen_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FristenErgebnis>, Integer, Hash)> fristen_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.fristen_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FristenErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling FristenApi->fristen_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bundesland** | **String** |  | [optional] |
| **voranmeldungsrhythmus** | **String** |  | [optional] |
| **dauerfristverlaengerung** | **Boolean** |  | [optional] |
| **est_aktiv** | **Boolean** |  | [optional] |
| **gewst_aktiv** | **Boolean** |  | [optional] |
| **monate** | **Integer** |  | [optional] |

### Return type

[**FristenErgebnis**](FristenErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

