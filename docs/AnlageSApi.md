# SimplebillyApi::AnlageSApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**anlage_s_api**](AnlageSApi.md#anlage_s_api) | **GET** /api/v1/bookkeeping/anlage-s |  |


## anlage_s_api

> <AnlageSErgebnis> anlage_s_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AnlageSApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.anlage_s_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AnlageSApi->anlage_s_api: #{e}"
end
```

#### Using the anlage_s_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AnlageSErgebnis>, Integer, Hash)> anlage_s_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.anlage_s_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AnlageSErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AnlageSApi->anlage_s_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**AnlageSErgebnis**](AnlageSErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

