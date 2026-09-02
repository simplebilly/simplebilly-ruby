# SimplebillyApi::GewerbesteuerApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**gewerbesteuer_api**](GewerbesteuerApi.md#gewerbesteuer_api) | **GET** /api/v1/bookkeeping/gewerbesteuer |  |


## gewerbesteuer_api

> <GewerbesteuerErgebnis> gewerbesteuer_api(year, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GewerbesteuerApi.new
year = 56 # Integer | 
opts = {
  hebesatz: 'hebesatz_example', # String | 
  gewerbeertrag: 'gewerbeertrag_example', # String | 
  country: 'country_example', # String | 
  gemeindeschluessel: 'gemeindeschluessel_example' # String | 
}

begin
  
  result = api_instance.gewerbesteuer_api(year, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GewerbesteuerApi->gewerbesteuer_api: #{e}"
end
```

#### Using the gewerbesteuer_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GewerbesteuerErgebnis>, Integer, Hash)> gewerbesteuer_api_with_http_info(year, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.gewerbesteuer_api_with_http_info(year, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GewerbesteuerErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GewerbesteuerApi->gewerbesteuer_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |
| **hebesatz** | **String** |  | [optional] |
| **gewerbeertrag** | **String** |  | [optional] |
| **country** | **String** |  | [optional] |
| **gemeindeschluessel** | **String** |  | [optional] |

### Return type

[**GewerbesteuerErgebnis**](GewerbesteuerErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

