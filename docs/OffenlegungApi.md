# SimplebillyApi::OffenlegungApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**offenlegung_api**](OffenlegungApi.md#offenlegung_api) | **GET** /api/v1/bookkeeping/offenlegung |  |


## offenlegung_api

> <OffenlegungReport> offenlegung_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OffenlegungApi.new

begin
  
  result = api_instance.offenlegung_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OffenlegungApi->offenlegung_api: #{e}"
end
```

#### Using the offenlegung_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OffenlegungReport>, Integer, Hash)> offenlegung_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.offenlegung_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OffenlegungReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OffenlegungApi->offenlegung_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**OffenlegungReport**](OffenlegungReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

