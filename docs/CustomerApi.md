# SimplebillyApi::CustomerApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_customer**](CustomerApi.md#create_customer) | **POST** /api/v1/customers |  |
| [**customer_restore**](CustomerApi.md#customer_restore) | **POST** /api/v1/customers/{customer_id}/restore |  |
| [**delete_customer**](CustomerApi.md#delete_customer) | **DELETE** /api/v1/customers/{customer_id} |  |
| [**get_customer**](CustomerApi.md#get_customer) | **GET** /api/v1/customers/{customer_id} |  |
| [**get_customers**](CustomerApi.md#get_customers) | **GET** /api/v1/customers/ |  |
| [**update_customer**](CustomerApi.md#update_customer) | **PUT** /api/v1/customers/{customer_id} |  |


## create_customer

> <Customer> create_customer(customer_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerApi.new
customer_create = SimplebillyApi::CustomerCreate.new({name: 'name_example'}) # CustomerCreate | 

begin
  
  result = api_instance.create_customer(customer_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->create_customer: #{e}"
end
```

#### Using the create_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> create_customer_with_http_info(customer_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_customer_with_http_info(customer_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->create_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_create** | [**CustomerCreate**](CustomerCreate.md) |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## customer_restore

> <Customer> customer_restore(customer_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerApi.new
customer_id = 'customer_id_example' # String | 

begin
  
  result = api_instance.customer_restore(customer_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->customer_restore: #{e}"
end
```

#### Using the customer_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> customer_restore_with_http_info(customer_id)

```ruby
begin
  
  data, status_code, headers = api_instance.customer_restore_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->customer_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_customer

> delete_customer(customer_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerApi.new
customer_id = 'customer_id_example' # String | 

begin
  
  api_instance.delete_customer(customer_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->delete_customer: #{e}"
end
```

#### Using the delete_customer_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_customer_with_http_info(customer_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->delete_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_customer

> <Customer> get_customer(customer_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerApi.new
customer_id = 'customer_id_example' # String | 

begin
  
  result = api_instance.get_customer(customer_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->get_customer: #{e}"
end
```

#### Using the get_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> get_customer_with_http_info(customer_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->get_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_customers

> <Array<Customer>> get_customers(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_customers(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->get_customers: #{e}"
end
```

#### Using the get_customers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Customer>>, Integer, Hash)> get_customers_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_customers_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Customer>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->get_customers_with_http_info: #{e}"
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

[**Array&lt;Customer&gt;**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_customer

> <Customer> update_customer(customer_id, customer_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerApi.new
customer_id = 'customer_id_example' # String | 
customer_update = SimplebillyApi::CustomerUpdate.new # CustomerUpdate | 

begin
  
  result = api_instance.update_customer(customer_id, customer_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->update_customer: #{e}"
end
```

#### Using the update_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customer>, Integer, Hash)> update_customer_with_http_info(customer_id, customer_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_customer_with_http_info(customer_id, customer_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customer>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerApi->update_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |
| **customer_update** | [**CustomerUpdate**](CustomerUpdate.md) |  |  |

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

