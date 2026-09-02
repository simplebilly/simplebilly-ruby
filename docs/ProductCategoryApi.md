# SimplebillyApi::ProductCategoryApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_product_category**](ProductCategoryApi.md#create_product_category) | **POST** /api/v1/product-categories |  |
| [**delete_product_category**](ProductCategoryApi.md#delete_product_category) | **DELETE** /api/v1/product-categories/{category_id} |  |
| [**get_product_category**](ProductCategoryApi.md#get_product_category) | **GET** /api/v1/product-categories/{category_id} |  |
| [**list_product_categories**](ProductCategoryApi.md#list_product_categories) | **GET** /api/v1/product-categories |  |
| [**update_product_category**](ProductCategoryApi.md#update_product_category) | **PUT** /api/v1/product-categories/{category_id} |  |


## create_product_category

> <ProductCategory> create_product_category(product_category)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductCategoryApi.new
product_category = SimplebillyApi::ProductCategory.new({name: 'name_example', sort_order: 37}) # ProductCategory | 

begin
  
  result = api_instance.create_product_category(product_category)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->create_product_category: #{e}"
end
```

#### Using the create_product_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductCategory>, Integer, Hash)> create_product_category_with_http_info(product_category)

```ruby
begin
  
  data, status_code, headers = api_instance.create_product_category_with_http_info(product_category)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductCategory>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->create_product_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_category** | [**ProductCategory**](ProductCategory.md) |  |  |

### Return type

[**ProductCategory**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_product_category

> delete_product_category(category_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductCategoryApi.new
category_id = 'category_id_example' # String | 

begin
  
  api_instance.delete_product_category(category_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->delete_product_category: #{e}"
end
```

#### Using the delete_product_category_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_product_category_with_http_info(category_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_product_category_with_http_info(category_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->delete_product_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_product_category

> <ProductCategory> get_product_category(category_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductCategoryApi.new
category_id = 'category_id_example' # String | 

begin
  
  result = api_instance.get_product_category(category_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->get_product_category: #{e}"
end
```

#### Using the get_product_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductCategory>, Integer, Hash)> get_product_category_with_http_info(category_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_product_category_with_http_info(category_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductCategory>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->get_product_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |

### Return type

[**ProductCategory**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_product_categories

> <Array<ProductCategory>> list_product_categories



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductCategoryApi.new

begin
  
  result = api_instance.list_product_categories
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->list_product_categories: #{e}"
end
```

#### Using the list_product_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProductCategory>>, Integer, Hash)> list_product_categories_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_product_categories_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProductCategory>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->list_product_categories_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;ProductCategory&gt;**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_product_category

> <ProductCategory> update_product_category(category_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductCategoryApi.new
category_id = 'category_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_product_category(category_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->update_product_category: #{e}"
end
```

#### Using the update_product_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductCategory>, Integer, Hash)> update_product_category_with_http_info(category_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_product_category_with_http_info(category_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductCategory>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductCategoryApi->update_product_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**ProductCategory**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

