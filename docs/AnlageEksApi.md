# SimplebillyApi::AnlageEksApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**eks_api**](AnlageEksApi.md#eks_api) | **GET** /api/v1/bookkeeping/eks |  |


## eks_api

> <EksErgebnis> eks_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AnlageEksApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.eks_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AnlageEksApi->eks_api: #{e}"
end
```

#### Using the eks_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EksErgebnis>, Integer, Hash)> eks_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.eks_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EksErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AnlageEksApi->eks_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**EksErgebnis**](EksErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

