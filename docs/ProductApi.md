# SimplebillyApi::ProductApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_product_api**](ProductApi.md#create_product_api) | **POST** /api/v1/products |  |
| [**delete_product_api**](ProductApi.md#delete_product_api) | **DELETE** /api/v1/products/{product_id} |  |
| [**get_product_api**](ProductApi.md#get_product_api) | **GET** /api/v1/products/{product_id} |  |
| [**get_product_stock_api**](ProductApi.md#get_product_stock_api) | **GET** /api/v1/products/{product_id}/stock |  |
| [**get_products_api**](ProductApi.md#get_products_api) | **GET** /api/v1/products/ |  |
| [**list_low_stock_products_api**](ProductApi.md#list_low_stock_products_api) | **GET** /api/v1/products/low-stock |  |
| [**product_restore**](ProductApi.md#product_restore) | **POST** /api/v1/products/{product_id}/restore |  |
| [**update_product_api**](ProductApi.md#update_product_api) | **PUT** /api/v1/products/{product_id} |  |
| [**update_product_stock_api**](ProductApi.md#update_product_stock_api) | **PUT** /api/v1/products/{product_id}/stock |  |


## create_product_api

> <Product> create_product_api(product_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
product_create = SimplebillyApi::ProductCreate.new({name: 'name_example', product_code: 'product_code_example', sku: 'sku_example'}) # ProductCreate | 

begin
  
  result = api_instance.create_product_api(product_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->create_product_api: #{e}"
end
```

#### Using the create_product_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> create_product_api_with_http_info(product_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_product_api_with_http_info(product_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->create_product_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_create** | [**ProductCreate**](ProductCreate.md) |  |  |

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_product_api

> delete_product_api(product_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_product_api(product_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->delete_product_api: #{e}"
end
```

#### Using the delete_product_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_product_api_with_http_info(product_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_product_api_with_http_info(product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->delete_product_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_product_api

> <Product> get_product_api(product_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_product_api(product_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->get_product_api: #{e}"
end
```

#### Using the get_product_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> get_product_api_with_http_info(product_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_product_api_with_http_info(product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->get_product_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_product_stock_api

> <ProductStock> get_product_stock_api(product_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_product_stock_api(product_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->get_product_stock_api: #{e}"
end
```

#### Using the get_product_stock_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductStock>, Integer, Hash)> get_product_stock_api_with_http_info(product_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_product_stock_api_with_http_info(product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductStock>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->get_product_stock_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |

### Return type

[**ProductStock**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_products_api

> <Array<Product>> get_products_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_products_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->get_products_api: #{e}"
end
```

#### Using the get_products_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Product>>, Integer, Hash)> get_products_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_products_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Product>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->get_products_api_with_http_info: #{e}"
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

[**Array&lt;Product&gt;**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_low_stock_products_api

> <Array<ProductStock>> list_low_stock_products_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
opts = {
  threshold: 789 # Integer | 
}

begin
  
  result = api_instance.list_low_stock_products_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->list_low_stock_products_api: #{e}"
end
```

#### Using the list_low_stock_products_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProductStock>>, Integer, Hash)> list_low_stock_products_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_low_stock_products_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProductStock>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->list_low_stock_products_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **threshold** | **Integer** |  | [optional] |

### Return type

[**Array&lt;ProductStock&gt;**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## product_restore

> <Product> product_restore(product_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.product_restore(product_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->product_restore: #{e}"
end
```

#### Using the product_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> product_restore_with_http_info(product_id)

```ruby
begin
  
  data, status_code, headers = api_instance.product_restore_with_http_info(product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->product_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_product_api

> <Product> update_product_api(product_id, product_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
product_update = SimplebillyApi::ProductUpdate.new # ProductUpdate | 

begin
  
  result = api_instance.update_product_api(product_id, product_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->update_product_api: #{e}"
end
```

#### Using the update_product_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> update_product_api_with_http_info(product_id, product_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_product_api_with_http_info(product_id, product_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->update_product_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **product_update** | [**ProductUpdate**](ProductUpdate.md) |  |  |

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_product_stock_api

> <ProductStock> update_product_stock_api(product_id, stock_update_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
stock_update_request = SimplebillyApi::StockUpdateRequest.new({quantity: 3.56}) # StockUpdateRequest | 

begin
  
  result = api_instance.update_product_stock_api(product_id, stock_update_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->update_product_stock_api: #{e}"
end
```

#### Using the update_product_stock_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductStock>, Integer, Hash)> update_product_stock_api_with_http_info(product_id, stock_update_request)

```ruby
begin
  
  data, status_code, headers = api_instance.update_product_stock_api_with_http_info(product_id, stock_update_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductStock>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductApi->update_product_stock_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **stock_update_request** | [**StockUpdateRequest**](StockUpdateRequest.md) |  |  |

### Return type

[**ProductStock**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

