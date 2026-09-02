# SimplebillyApi::PaymentGatewayApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_payment_gateway_api**](PaymentGatewayApi.md#create_payment_gateway_api) | **POST** /api/v1/payment-gateways |  |
| [**delete_payment_gateway_api**](PaymentGatewayApi.md#delete_payment_gateway_api) | **DELETE** /api/v1/payment-gateways/{gateway_id} |  |
| [**list_payment_gateways_api**](PaymentGatewayApi.md#list_payment_gateways_api) | **GET** /api/v1/payment-gateways/ |  |
| [**oauth_authorize_api**](PaymentGatewayApi.md#oauth_authorize_api) | **POST** /api/v1/payment-gateways/oauth/authorize |  |
| [**oauth_callback_api**](PaymentGatewayApi.md#oauth_callback_api) | **POST** /api/v1/payment-gateways/oauth/callback |  |
| [**update_payment_gateway_api**](PaymentGatewayApi.md#update_payment_gateway_api) | **PUT** /api/v1/payment-gateways/{gateway_id} |  |


## create_payment_gateway_api

> <PaymentGateway> create_payment_gateway_api(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentGatewayApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.create_payment_gateway_api(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->create_payment_gateway_api: #{e}"
end
```

#### Using the create_payment_gateway_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentGateway>, Integer, Hash)> create_payment_gateway_api_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.create_payment_gateway_api_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentGateway>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->create_payment_gateway_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_payment_gateway_api

> delete_payment_gateway_api(gateway_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentGatewayApi.new
gateway_id = 'gateway_id_example' # String | 

begin
  
  api_instance.delete_payment_gateway_api(gateway_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->delete_payment_gateway_api: #{e}"
end
```

#### Using the delete_payment_gateway_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_payment_gateway_api_with_http_info(gateway_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_payment_gateway_api_with_http_info(gateway_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->delete_payment_gateway_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gateway_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_payment_gateways_api

> <Array<PaymentGateway>> list_payment_gateways_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentGatewayApi.new

begin
  
  result = api_instance.list_payment_gateways_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->list_payment_gateways_api: #{e}"
end
```

#### Using the list_payment_gateways_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PaymentGateway>>, Integer, Hash)> list_payment_gateways_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_payment_gateways_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PaymentGateway>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->list_payment_gateways_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;PaymentGateway&gt;**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## oauth_authorize_api

> <GatewayOAuthAuthorizeResponse> oauth_authorize_api(gateway_o_auth_authorize_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentGatewayApi.new
gateway_o_auth_authorize_request = SimplebillyApi::GatewayOAuthAuthorizeRequest.new({gateway_type: 'gateway_type_example', redirect_uri: 'redirect_uri_example'}) # GatewayOAuthAuthorizeRequest | 

begin
  
  result = api_instance.oauth_authorize_api(gateway_o_auth_authorize_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->oauth_authorize_api: #{e}"
end
```

#### Using the oauth_authorize_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GatewayOAuthAuthorizeResponse>, Integer, Hash)> oauth_authorize_api_with_http_info(gateway_o_auth_authorize_request)

```ruby
begin
  
  data, status_code, headers = api_instance.oauth_authorize_api_with_http_info(gateway_o_auth_authorize_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GatewayOAuthAuthorizeResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->oauth_authorize_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gateway_o_auth_authorize_request** | [**GatewayOAuthAuthorizeRequest**](GatewayOAuthAuthorizeRequest.md) |  |  |

### Return type

[**GatewayOAuthAuthorizeResponse**](GatewayOAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## oauth_callback_api

> <PaymentGateway> oauth_callback_api(gateway_o_auth_callback_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentGatewayApi.new
gateway_o_auth_callback_request = SimplebillyApi::GatewayOAuthCallbackRequest.new({code: 'code_example', gateway_type: 'gateway_type_example', redirect_uri: 'redirect_uri_example', state: 'state_example'}) # GatewayOAuthCallbackRequest | 

begin
  
  result = api_instance.oauth_callback_api(gateway_o_auth_callback_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->oauth_callback_api: #{e}"
end
```

#### Using the oauth_callback_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentGateway>, Integer, Hash)> oauth_callback_api_with_http_info(gateway_o_auth_callback_request)

```ruby
begin
  
  data, status_code, headers = api_instance.oauth_callback_api_with_http_info(gateway_o_auth_callback_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentGateway>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->oauth_callback_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gateway_o_auth_callback_request** | [**GatewayOAuthCallbackRequest**](GatewayOAuthCallbackRequest.md) |  |  |

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_payment_gateway_api

> <PaymentGateway> update_payment_gateway_api(gateway_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentGatewayApi.new
gateway_id = 'gateway_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_payment_gateway_api(gateway_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->update_payment_gateway_api: #{e}"
end
```

#### Using the update_payment_gateway_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentGateway>, Integer, Hash)> update_payment_gateway_api_with_http_info(gateway_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_payment_gateway_api_with_http_info(gateway_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentGateway>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentGatewayApi->update_payment_gateway_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gateway_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

