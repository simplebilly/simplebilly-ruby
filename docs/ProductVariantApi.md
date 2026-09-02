# SimplebillyApi::ProductVariantApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_product_variant**](ProductVariantApi.md#create_product_variant) | **POST** /api/v1/product-variants |  |
| [**delete_product_variant**](ProductVariantApi.md#delete_product_variant) | **DELETE** /api/v1/product-variants/{variant_id} |  |
| [**generate_product_variants**](ProductVariantApi.md#generate_product_variants) | **POST** /api/v1/product-variants/generate |  |
| [**get_product_variant**](ProductVariantApi.md#get_product_variant) | **GET** /api/v1/product-variants/{variant_id} |  |
| [**list_product_variants**](ProductVariantApi.md#list_product_variants) | **GET** /api/v1/product-variants/ |  |
| [**update_product_variant**](ProductVariantApi.md#update_product_variant) | **PUT** /api/v1/product-variants/{variant_id} |  |


## create_product_variant

> <ProductVariant> create_product_variant(product_variant)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductVariantApi.new
product_variant = SimplebillyApi::ProductVariant.new({product_id: 'product_id_example', sku: 'sku_example'}) # ProductVariant | 

begin
  
  result = api_instance.create_product_variant(product_variant)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->create_product_variant: #{e}"
end
```

#### Using the create_product_variant_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductVariant>, Integer, Hash)> create_product_variant_with_http_info(product_variant)

```ruby
begin
  
  data, status_code, headers = api_instance.create_product_variant_with_http_info(product_variant)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductVariant>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->create_product_variant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_variant** | [**ProductVariant**](ProductVariant.md) |  |  |

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_product_variant

> delete_product_variant(variant_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductVariantApi.new
variant_id = 'variant_id_example' # String | 

begin
  
  api_instance.delete_product_variant(variant_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->delete_product_variant: #{e}"
end
```

#### Using the delete_product_variant_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_product_variant_with_http_info(variant_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_product_variant_with_http_info(variant_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->delete_product_variant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **variant_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## generate_product_variants

> <Array<ProductVariant>> generate_product_variants(generate_variants_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductVariantApi.new
generate_variants_request = SimplebillyApi::GenerateVariantsRequest.new({product_id: 'product_id_example'}) # GenerateVariantsRequest | 

begin
  
  result = api_instance.generate_product_variants(generate_variants_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->generate_product_variants: #{e}"
end
```

#### Using the generate_product_variants_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProductVariant>>, Integer, Hash)> generate_product_variants_with_http_info(generate_variants_request)

```ruby
begin
  
  data, status_code, headers = api_instance.generate_product_variants_with_http_info(generate_variants_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProductVariant>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->generate_product_variants_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **generate_variants_request** | [**GenerateVariantsRequest**](GenerateVariantsRequest.md) |  |  |

### Return type

[**Array&lt;ProductVariant&gt;**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_product_variant

> <ProductVariant> get_product_variant(variant_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductVariantApi.new
variant_id = 'variant_id_example' # String | 

begin
  
  result = api_instance.get_product_variant(variant_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->get_product_variant: #{e}"
end
```

#### Using the get_product_variant_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductVariant>, Integer, Hash)> get_product_variant_with_http_info(variant_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_product_variant_with_http_info(variant_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductVariant>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->get_product_variant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **variant_id** | **String** |  |  |

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_product_variants

> <Array<ProductVariant>> list_product_variants(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductVariantApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  product_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  is_active: true # Boolean | 
}

begin
  
  result = api_instance.list_product_variants(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->list_product_variants: #{e}"
end
```

#### Using the list_product_variants_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProductVariant>>, Integer, Hash)> list_product_variants_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_product_variants_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProductVariant>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->list_product_variants_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |

### Return type

[**Array&lt;ProductVariant&gt;**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_product_variant

> <ProductVariant> update_product_variant(variant_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductVariantApi.new
variant_id = 'variant_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_product_variant(variant_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->update_product_variant: #{e}"
end
```

#### Using the update_product_variant_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductVariant>, Integer, Hash)> update_product_variant_with_http_info(variant_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_product_variant_with_http_info(variant_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductVariant>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductVariantApi->update_product_variant_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **variant_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

