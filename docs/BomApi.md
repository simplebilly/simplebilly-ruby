# SimplebillyApi::BomApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_bom**](BomApi.md#create_bom) | **POST** /api/v1/boms |  |
| [**delete_bom**](BomApi.md#delete_bom) | **DELETE** /api/v1/boms/{bom_id} |  |
| [**get_bom**](BomApi.md#get_bom) | **GET** /api/v1/boms/{bom_id} |  |
| [**list_boms**](BomApi.md#list_boms) | **GET** /api/v1/boms/ |  |
| [**update_bom**](BomApi.md#update_bom) | **PUT** /api/v1/boms/{bom_id} |  |


## create_bom

> <Bom> create_bom(bom_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BomApi.new
bom_create = SimplebillyApi::BomCreate.new({name: 'name_example', product_id: 'product_id_example'}) # BomCreate | 

begin
  
  result = api_instance.create_bom(bom_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->create_bom: #{e}"
end
```

#### Using the create_bom_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Bom>, Integer, Hash)> create_bom_with_http_info(bom_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_bom_with_http_info(bom_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Bom>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->create_bom_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bom_create** | [**BomCreate**](BomCreate.md) |  |  |

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_bom

> delete_bom(bom_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BomApi.new
bom_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_bom(bom_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->delete_bom: #{e}"
end
```

#### Using the delete_bom_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_bom_with_http_info(bom_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_bom_with_http_info(bom_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->delete_bom_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bom_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_bom

> <Bom> get_bom(bom_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BomApi.new
bom_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_bom(bom_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->get_bom: #{e}"
end
```

#### Using the get_bom_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Bom>, Integer, Hash)> get_bom_with_http_info(bom_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_bom_with_http_info(bom_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Bom>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->get_bom_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bom_id** | **String** |  |  |

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_boms

> <Array<Bom>> list_boms(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BomApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  product_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | Filter by finished product id.
}

begin
  
  result = api_instance.list_boms(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->list_boms: #{e}"
end
```

#### Using the list_boms_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Bom>>, Integer, Hash)> list_boms_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_boms_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Bom>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->list_boms_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **product_id** | **String** | Filter by finished product id. | [optional] |

### Return type

[**Array&lt;Bom&gt;**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_bom

> <Bom> update_bom(bom_id, bom_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BomApi.new
bom_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
bom_update = SimplebillyApi::BomUpdate.new # BomUpdate | 

begin
  
  result = api_instance.update_bom(bom_id, bom_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->update_bom: #{e}"
end
```

#### Using the update_bom_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Bom>, Integer, Hash)> update_bom_with_http_info(bom_id, bom_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_bom_with_http_info(bom_id, bom_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Bom>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BomApi->update_bom_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bom_id** | **String** |  |  |
| **bom_update** | [**BomUpdate**](BomUpdate.md) |  |  |

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

