# SimplebillyApi::PublicReturnsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_public_return_status**](PublicReturnsApi.md#get_public_return_status) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches. |
| [**list_public_returns**](PublicReturnsApi.md#list_public_returns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth). |
| [**request_public_return**](PublicReturnsApi.md#request_public_return) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth). |


## get_public_return_status

> <PublicReturnStatusResponse> get_public_return_status(email, opts)

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PublicReturnsApi.new
email = 'email_example' # String | 
opts = {
  return_number: 'return_number_example', # String | Either return_number or return_order_id must be provided.
  return_order_id: 'return_order_id_example', # String | 
  order_number: 'order_number_example' # String | 
}

begin
  # Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.
  result = api_instance.get_public_return_status(email, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PublicReturnsApi->get_public_return_status: #{e}"
end
```

#### Using the get_public_return_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicReturnStatusResponse>, Integer, Hash)> get_public_return_status_with_http_info(email, opts)

```ruby
begin
  # Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.
  data, status_code, headers = api_instance.get_public_return_status_with_http_info(email, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicReturnStatusResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PublicReturnsApi->get_public_return_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** |  |  |
| **return_number** | **String** | Either return_number or return_order_id must be provided. | [optional] |
| **return_order_id** | **String** |  | [optional] |
| **order_number** | **String** |  | [optional] |

### Return type

[**PublicReturnStatusResponse**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_public_returns

> <Array<PublicReturnStatusResponse>> list_public_returns(order_number, email)

List all returns for an order (public, no auth).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PublicReturnsApi.new
order_number = 'order_number_example' # String | 
email = 'email_example' # String | 

begin
  # List all returns for an order (public, no auth).
  result = api_instance.list_public_returns(order_number, email)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PublicReturnsApi->list_public_returns: #{e}"
end
```

#### Using the list_public_returns_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PublicReturnStatusResponse>>, Integer, Hash)> list_public_returns_with_http_info(order_number, email)

```ruby
begin
  # List all returns for an order (public, no auth).
  data, status_code, headers = api_instance.list_public_returns_with_http_info(order_number, email)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PublicReturnStatusResponse>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PublicReturnsApi->list_public_returns_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |
| **email** | **String** |  |  |

### Return type

[**Array&lt;PublicReturnStatusResponse&gt;**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## request_public_return

> <PublicReturnResponse> request_public_return(public_return_request)

Customer requests a return for an order (public, no auth).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PublicReturnsApi.new
public_return_request = SimplebillyApi::PublicReturnRequest.new({email: 'email_example', items: [SimplebillyApi::PublicReturnItem.new({product_id: 'product_id_example', quantity: 3.56})], order_number: 'order_number_example'}) # PublicReturnRequest | 

begin
  # Customer requests a return for an order (public, no auth).
  result = api_instance.request_public_return(public_return_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PublicReturnsApi->request_public_return: #{e}"
end
```

#### Using the request_public_return_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicReturnResponse>, Integer, Hash)> request_public_return_with_http_info(public_return_request)

```ruby
begin
  # Customer requests a return for an order (public, no auth).
  data, status_code, headers = api_instance.request_public_return_with_http_info(public_return_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicReturnResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PublicReturnsApi->request_public_return_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **public_return_request** | [**PublicReturnRequest**](PublicReturnRequest.md) |  |  |

### Return type

[**PublicReturnResponse**](PublicReturnResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

