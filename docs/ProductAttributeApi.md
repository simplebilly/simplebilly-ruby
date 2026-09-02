# SimplebillyApi::ProductAttributeApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_product_attribute**](ProductAttributeApi.md#create_product_attribute) | **POST** /api/v1/product-attributes |  |
| [**delete_product_attribute**](ProductAttributeApi.md#delete_product_attribute) | **DELETE** /api/v1/product-attributes/{attribute_id} |  |
| [**get_product_attribute**](ProductAttributeApi.md#get_product_attribute) | **GET** /api/v1/product-attributes/{attribute_id} |  |
| [**list_product_attributes**](ProductAttributeApi.md#list_product_attributes) | **GET** /api/v1/product-attributes/ |  |
| [**update_product_attribute**](ProductAttributeApi.md#update_product_attribute) | **PUT** /api/v1/product-attributes/{attribute_id} |  |


## create_product_attribute

> <ProductAttribute> create_product_attribute(product_attribute_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductAttributeApi.new
product_attribute_create = SimplebillyApi::ProductAttributeCreate.new({name: 'name_example', product_id: 'product_id_example', value: 'value_example'}) # ProductAttributeCreate | 

begin
  
  result = api_instance.create_product_attribute(product_attribute_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->create_product_attribute: #{e}"
end
```

#### Using the create_product_attribute_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductAttribute>, Integer, Hash)> create_product_attribute_with_http_info(product_attribute_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_product_attribute_with_http_info(product_attribute_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductAttribute>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->create_product_attribute_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_attribute_create** | [**ProductAttributeCreate**](ProductAttributeCreate.md) |  |  |

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_product_attribute

> delete_product_attribute(attribute_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductAttributeApi.new
attribute_id = 'attribute_id_example' # String | 

begin
  
  api_instance.delete_product_attribute(attribute_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->delete_product_attribute: #{e}"
end
```

#### Using the delete_product_attribute_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_product_attribute_with_http_info(attribute_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_product_attribute_with_http_info(attribute_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->delete_product_attribute_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attribute_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_product_attribute

> <ProductAttribute> get_product_attribute(attribute_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductAttributeApi.new
attribute_id = 'attribute_id_example' # String | 

begin
  
  result = api_instance.get_product_attribute(attribute_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->get_product_attribute: #{e}"
end
```

#### Using the get_product_attribute_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductAttribute>, Integer, Hash)> get_product_attribute_with_http_info(attribute_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_product_attribute_with_http_info(attribute_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductAttribute>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->get_product_attribute_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attribute_id** | **String** |  |  |

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_product_attributes

> <Array<ProductAttribute>> list_product_attributes(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductAttributeApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  product_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  is_filterable: true, # Boolean | 
  search: 'search_example' # String | 
}

begin
  
  result = api_instance.list_product_attributes(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->list_product_attributes: #{e}"
end
```

#### Using the list_product_attributes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProductAttribute>>, Integer, Hash)> list_product_attributes_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_product_attributes_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProductAttribute>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->list_product_attributes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **is_filterable** | **Boolean** |  | [optional] |
| **search** | **String** |  | [optional] |

### Return type

[**Array&lt;ProductAttribute&gt;**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_product_attribute

> <ProductAttribute> update_product_attribute(attribute_id, product_attribute_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductAttributeApi.new
attribute_id = 'attribute_id_example' # String | 
product_attribute_update = SimplebillyApi::ProductAttributeUpdate.new # ProductAttributeUpdate | 

begin
  
  result = api_instance.update_product_attribute(attribute_id, product_attribute_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->update_product_attribute: #{e}"
end
```

#### Using the update_product_attribute_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductAttribute>, Integer, Hash)> update_product_attribute_with_http_info(attribute_id, product_attribute_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_product_attribute_with_http_info(attribute_id, product_attribute_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductAttribute>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductAttributeApi->update_product_attribute_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attribute_id** | **String** |  |  |
| **product_attribute_update** | [**ProductAttributeUpdate**](ProductAttributeUpdate.md) |  |  |

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

