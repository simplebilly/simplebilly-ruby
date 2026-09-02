# SimplebillyApi::SuitabilityApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**shipping_suitability_api**](SuitabilityApi.md#shipping_suitability_api) | **POST** /api/v1/shipping/suitability |  |


## shipping_suitability_api

> <SuitabilityResult> shipping_suitability_api(suitability_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SuitabilityApi.new
suitability_request = SimplebillyApi::SuitabilityRequest.new({items: [SimplebillyApi::CartItemInput.new({product_id: 'product_id_example', quantity: 37})], recipient: SimplebillyApi::Address.new({city: 'city_example', country: 'country_example', name: 'name_example', street: 'street_example', street_number: 'street_number_example', zip: 'zip_example'}), sender: SimplebillyApi::Address.new({city: 'city_example', country: 'country_example', name: 'name_example', street: 'street_example', street_number: 'street_number_example', zip: 'zip_example'})}) # SuitabilityRequest | 

begin
  
  result = api_instance.shipping_suitability_api(suitability_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SuitabilityApi->shipping_suitability_api: #{e}"
end
```

#### Using the shipping_suitability_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SuitabilityResult>, Integer, Hash)> shipping_suitability_api_with_http_info(suitability_request)

```ruby
begin
  
  data, status_code, headers = api_instance.shipping_suitability_api_with_http_info(suitability_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SuitabilityResult>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SuitabilityApi->shipping_suitability_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **suitability_request** | [**SuitabilityRequest**](SuitabilityRequest.md) |  |  |

### Return type

[**SuitabilityResult**](SuitabilityResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

