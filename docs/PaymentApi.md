# SimplebillyApi::PaymentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_payment**](PaymentApi.md#create_payment) | **POST** /api/v1/payments |  |
| [**delete_payment**](PaymentApi.md#delete_payment) | **DELETE** /api/v1/payments/{id} |  |
| [**get_payment**](PaymentApi.md#get_payment) | **GET** /api/v1/payments/{id} |  |
| [**get_payments**](PaymentApi.md#get_payments) | **GET** /api/v1/payments/ |  |
| [**payment_restore**](PaymentApi.md#payment_restore) | **POST** /api/v1/payments/{id}/restore |  |
| [**update_payment**](PaymentApi.md#update_payment) | **PUT** /api/v1/payments/{id} |  |


## create_payment

> <Payment> create_payment(payment_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentApi.new
payment_create = SimplebillyApi::PaymentCreate.new # PaymentCreate | 

begin
  
  result = api_instance.create_payment(payment_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->create_payment: #{e}"
end
```

#### Using the create_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> create_payment_with_http_info(payment_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_payment_with_http_info(payment_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->create_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payment_create** | [**PaymentCreate**](PaymentCreate.md) |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_payment

> delete_payment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_payment(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->delete_payment: #{e}"
end
```

#### Using the delete_payment_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_payment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_payment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->delete_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_payment

> <Payment> get_payment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_payment(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->get_payment: #{e}"
end
```

#### Using the get_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> get_payment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_payment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->get_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_payments

> <Array<Payment>> get_payments(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_payments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->get_payments: #{e}"
end
```

#### Using the get_payments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Payment>>, Integer, Hash)> get_payments_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_payments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Payment>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->get_payments_with_http_info: #{e}"
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

[**Array&lt;Payment&gt;**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payment_restore

> <Payment> payment_restore(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.payment_restore(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->payment_restore: #{e}"
end
```

#### Using the payment_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> payment_restore_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payment_restore_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->payment_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_payment

> <Payment> update_payment(id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_payment(id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->update_payment: #{e}"
end
```

#### Using the update_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Payment>, Integer, Hash)> update_payment_with_http_info(id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_payment_with_http_info(id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Payment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentApi->update_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

