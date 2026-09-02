# SimplebillyApi::OrderApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_order_tags**](OrderApi.md#add_order_tags) | **POST** /api/v1/orders/{order_id}/tags |  |
| [**find_order_by_external_ref**](OrderApi.md#find_order_by_external_ref) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} |  |
| [**get_order**](OrderApi.md#get_order) | **GET** /api/v1/order/{order_number} |  |
| [**get_orders**](OrderApi.md#get_orders) | **GET** /api/v1/orders |  |
| [**patch_order**](OrderApi.md#patch_order) | **PATCH** /api/v1/orders/{order_id} |  |
| [**replace_order_tags**](OrderApi.md#replace_order_tags) | **PUT** /api/v1/orders/{order_id}/tags |  |
| [**update_order_state**](OrderApi.md#update_order_state) | **PUT** /api/v1/orders/{order_id}/state |  |


## add_order_tags

> <Order> add_order_tags(order_id, order_tags_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderApi.new
order_id = 'order_id_example' # String | 
order_tags_request = SimplebillyApi::OrderTagsRequest.new({tags: ['tags_example']}) # OrderTagsRequest | 

begin
  
  result = api_instance.add_order_tags(order_id, order_tags_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->add_order_tags: #{e}"
end
```

#### Using the add_order_tags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> add_order_tags_with_http_info(order_id, order_tags_request)

```ruby
begin
  
  data, status_code, headers = api_instance.add_order_tags_with_http_info(order_id, order_tags_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->add_order_tags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** |  |  |
| **order_tags_request** | [**OrderTagsRequest**](OrderTagsRequest.md) |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## find_order_by_external_ref

> <Order> find_order_by_external_ref(ext_ref)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderApi.new
ext_ref = 'ext_ref_example' # String | 

begin
  
  result = api_instance.find_order_by_external_ref(ext_ref)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->find_order_by_external_ref: #{e}"
end
```

#### Using the find_order_by_external_ref_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> find_order_by_external_ref_with_http_info(ext_ref)

```ruby
begin
  
  data, status_code, headers = api_instance.find_order_by_external_ref_with_http_info(ext_ref)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->find_order_by_external_ref_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ext_ref** | **String** |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_order

> <Order> get_order(order_number)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderApi.new
order_number = 'order_number_example' # String | 

begin
  
  result = api_instance.get_order(order_number)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->get_order: #{e}"
end
```

#### Using the get_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> get_order_with_http_info(order_number)

```ruby
begin
  
  data, status_code, headers = api_instance.get_order_with_http_info(order_number)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->get_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_orders

> <Array<Order>> get_orders(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_orders(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->get_orders: #{e}"
end
```

#### Using the get_orders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Order>>, Integer, Hash)> get_orders_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_orders_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Order>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->get_orders_with_http_info: #{e}"
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

[**Array&lt;Order&gt;**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_order

> <Order> patch_order(order_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderApi.new
order_id = 'order_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.patch_order(order_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->patch_order: #{e}"
end
```

#### Using the patch_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> patch_order_with_http_info(order_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.patch_order_with_http_info(order_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->patch_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## replace_order_tags

> <Order> replace_order_tags(order_id, order_tags_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderApi.new
order_id = 'order_id_example' # String | 
order_tags_request = SimplebillyApi::OrderTagsRequest.new({tags: ['tags_example']}) # OrderTagsRequest | 

begin
  
  result = api_instance.replace_order_tags(order_id, order_tags_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->replace_order_tags: #{e}"
end
```

#### Using the replace_order_tags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> replace_order_tags_with_http_info(order_id, order_tags_request)

```ruby
begin
  
  data, status_code, headers = api_instance.replace_order_tags_with_http_info(order_id, order_tags_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->replace_order_tags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** |  |  |
| **order_tags_request** | [**OrderTagsRequest**](OrderTagsRequest.md) |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_order_state

> <Order> update_order_state(order_id, order_state_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OrderApi.new
order_id = 'order_id_example' # String | 
order_state_update = SimplebillyApi::OrderStateUpdate.new({state: 'state_example'}) # OrderStateUpdate | 

begin
  
  result = api_instance.update_order_state(order_id, order_state_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->update_order_state: #{e}"
end
```

#### Using the update_order_state_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> update_order_state_with_http_info(order_id, order_state_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_order_state_with_http_info(order_id, order_state_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OrderApi->update_order_state_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** |  |  |
| **order_state_update** | [**OrderStateUpdate**](OrderStateUpdate.md) |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

