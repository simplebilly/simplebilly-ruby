# SimplebillyApi::ShippingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_credentials_api**](ShippingApi.md#get_credentials_api) | **GET** /api/v1/shipping/credentials |  |
| [**get_rates_api**](ShippingApi.md#get_rates_api) | **POST** /api/v1/shipping/rates |  |
| [**list_providers_api**](ShippingApi.md#list_providers_api) | **GET** /api/v1/shipping/providers |  |
| [**save_credentials_api**](ShippingApi.md#save_credentials_api) | **PUT** /api/v1/shipping/credentials |  |


## get_credentials_api

> <ShippingCredentials> get_credentials_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingApi.new

begin
  
  result = api_instance.get_credentials_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->get_credentials_api: #{e}"
end
```

#### Using the get_credentials_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingCredentials>, Integer, Hash)> get_credentials_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.get_credentials_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingCredentials>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->get_credentials_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_rates_api

> <RateResponse> get_rates_api(rate_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingApi.new
rate_request = SimplebillyApi::RateRequest.new({packages: [SimplebillyApi::Package.new({weight_kg: 3.56})], recipient: SimplebillyApi::Address.new({city: 'city_example', country: 'country_example', name: 'name_example', street: 'street_example', street_number: 'street_number_example', zip: 'zip_example'}), sender: SimplebillyApi::Address.new({city: 'city_example', country: 'country_example', name: 'name_example', street: 'street_example', street_number: 'street_number_example', zip: 'zip_example'})}) # RateRequest | 

begin
  
  result = api_instance.get_rates_api(rate_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->get_rates_api: #{e}"
end
```

#### Using the get_rates_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RateResponse>, Integer, Hash)> get_rates_api_with_http_info(rate_request)

```ruby
begin
  
  data, status_code, headers = api_instance.get_rates_api_with_http_info(rate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RateResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->get_rates_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rate_request** | [**RateRequest**](RateRequest.md) |  |  |

### Return type

[**RateResponse**](RateResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_providers_api

> <Array<ProviderInfo>> list_providers_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingApi.new

begin
  
  result = api_instance.list_providers_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->list_providers_api: #{e}"
end
```

#### Using the list_providers_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProviderInfo>>, Integer, Hash)> list_providers_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_providers_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProviderInfo>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->list_providers_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;ProviderInfo&gt;**](ProviderInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## save_credentials_api

> <ShippingCredentials> save_credentials_api(shipping_credentials)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingApi.new
shipping_credentials = SimplebillyApi::ShippingCredentials.new # ShippingCredentials | 

begin
  
  result = api_instance.save_credentials_api(shipping_credentials)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->save_credentials_api: #{e}"
end
```

#### Using the save_credentials_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingCredentials>, Integer, Hash)> save_credentials_api_with_http_info(shipping_credentials)

```ruby
begin
  
  data, status_code, headers = api_instance.save_credentials_api_with_http_info(shipping_credentials)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingCredentials>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingApi->save_credentials_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipping_credentials** | [**ShippingCredentials**](ShippingCredentials.md) |  |  |

### Return type

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

