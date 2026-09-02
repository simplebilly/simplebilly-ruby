# SimplebillyApi::OrderConfirmationApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_confirmation**](OrderConfirmationApi.md#create_confirmation) | **POST** /api/v1/order-confirmations |  |
| [**delete_confirmation**](OrderConfirmationApi.md#delete_confirmation) | **DELETE** /api/v1/order-confirmations/{confirmation_id} |  |
| [**download_confirmation_pdf**](OrderConfirmationApi.md#download_confirmation_pdf) | **GET** /api/v1/order-confirmations/{confirmation_id}/pdf |  |
| [**get_confirmation**](OrderConfirmationApi.md#get_confirmation) | **GET** /api/v1/order-confirmations/{confirmation_id} |  |
| [**list_confirmations**](OrderConfirmationApi.md#list_confirmations) | **GET** /api/v1/order-confirmations/ |  |
| [**orderconfirmation_restore**](OrderConfirmationApi.md#orderconfirmation_restore) | **POST** /api/v1/order-confirmations/{confirmation_id}/restore |  |
| [**pursue_confirmation**](OrderConfirmationApi.md#pursue_confirmation) | **POST** /api/v1/order-confirmations/{confirmation_id}/pursue |  |


## create_confirmation

> <OrderConfirmation> create_confirmation(order_confirmation_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderConfirmationApi.new
order_confirmation_create = SimplebillyApi::OrderConfirmationCreate.new({currency: 'currency_example', voucher_date: Date.today, voucher_status: SimplebillyApi::VoucherStatus::OPEN}) # OrderConfirmationCreate | 

begin
  
  result = api_instance.create_confirmation(order_confirmation_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->create_confirmation: #{e}"
end
```

#### Using the create_confirmation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrderConfirmation>, Integer, Hash)> create_confirmation_with_http_info(order_confirmation_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_confirmation_with_http_info(order_confirmation_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrderConfirmation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->create_confirmation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_confirmation_create** | [**OrderConfirmationCreate**](OrderConfirmationCreate.md) |  |  |

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_confirmation

> delete_confirmation(confirmation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderConfirmationApi.new
confirmation_id = 'confirmation_id_example' # String | 

begin
  
  api_instance.delete_confirmation(confirmation_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->delete_confirmation: #{e}"
end
```

#### Using the delete_confirmation_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_confirmation_with_http_info(confirmation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_confirmation_with_http_info(confirmation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->delete_confirmation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **confirmation_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_confirmation_pdf

> download_confirmation_pdf(confirmation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderConfirmationApi.new
confirmation_id = 'confirmation_id_example' # String | 

begin
  
  api_instance.download_confirmation_pdf(confirmation_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->download_confirmation_pdf: #{e}"
end
```

#### Using the download_confirmation_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> download_confirmation_pdf_with_http_info(confirmation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.download_confirmation_pdf_with_http_info(confirmation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->download_confirmation_pdf_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **confirmation_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json


## get_confirmation

> <OrderConfirmation> get_confirmation(confirmation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderConfirmationApi.new
confirmation_id = 'confirmation_id_example' # String | 

begin
  
  result = api_instance.get_confirmation(confirmation_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->get_confirmation: #{e}"
end
```

#### Using the get_confirmation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrderConfirmation>, Integer, Hash)> get_confirmation_with_http_info(confirmation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_confirmation_with_http_info(confirmation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrderConfirmation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->get_confirmation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **confirmation_id** | **String** |  |  |

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_confirmations

> <Array<OrderConfirmation>> list_confirmations(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderConfirmationApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.list_confirmations(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->list_confirmations: #{e}"
end
```

#### Using the list_confirmations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<OrderConfirmation>>, Integer, Hash)> list_confirmations_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_confirmations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<OrderConfirmation>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->list_confirmations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **include_deleted** | **Boolean** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] |

### Return type

[**Array&lt;OrderConfirmation&gt;**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## orderconfirmation_restore

> <OrderConfirmation> orderconfirmation_restore(confirmation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderConfirmationApi.new
confirmation_id = 'confirmation_id_example' # String | 

begin
  
  result = api_instance.orderconfirmation_restore(confirmation_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->orderconfirmation_restore: #{e}"
end
```

#### Using the orderconfirmation_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrderConfirmation>, Integer, Hash)> orderconfirmation_restore_with_http_info(confirmation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.orderconfirmation_restore_with_http_info(confirmation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrderConfirmation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->orderconfirmation_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **confirmation_id** | **String** |  |  |

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pursue_confirmation

> <DeliveryNote> pursue_confirmation(confirmation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderConfirmationApi.new
confirmation_id = 'confirmation_id_example' # String | 

begin
  
  result = api_instance.pursue_confirmation(confirmation_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->pursue_confirmation: #{e}"
end
```

#### Using the pursue_confirmation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryNote>, Integer, Hash)> pursue_confirmation_with_http_info(confirmation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.pursue_confirmation_with_http_info(confirmation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryNote>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderConfirmationApi->pursue_confirmation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **confirmation_id** | **String** |  |  |

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

