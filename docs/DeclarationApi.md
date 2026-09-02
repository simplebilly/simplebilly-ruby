# SimplebillyApi::DeclarationApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_declaration**](DeclarationApi.md#create_declaration) | **POST** /api/v1/declarations |  |
| [**declaration_restore**](DeclarationApi.md#declaration_restore) | **POST** /api/v1/declarations/{id}/restore |  |
| [**delete_declaration**](DeclarationApi.md#delete_declaration) | **DELETE** /api/v1/declarations/{id} |  |
| [**get_declaration**](DeclarationApi.md#get_declaration) | **GET** /api/v1/declarations/{id} |  |
| [**get_declarations**](DeclarationApi.md#get_declarations) | **GET** /api/v1/declarations/ |  |
| [**update_declaration**](DeclarationApi.md#update_declaration) | **PUT** /api/v1/declarations/{id} |  |


## create_declaration

> <Declaration> create_declaration(declaration_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeclarationApi.new
declaration_create = SimplebillyApi::DeclarationCreate.new # DeclarationCreate | 

begin
  
  result = api_instance.create_declaration(declaration_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->create_declaration: #{e}"
end
```

#### Using the create_declaration_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Declaration>, Integer, Hash)> create_declaration_with_http_info(declaration_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_declaration_with_http_info(declaration_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Declaration>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->create_declaration_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **declaration_create** | [**DeclarationCreate**](DeclarationCreate.md) |  |  |

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## declaration_restore

> <Declaration> declaration_restore(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeclarationApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.declaration_restore(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->declaration_restore: #{e}"
end
```

#### Using the declaration_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Declaration>, Integer, Hash)> declaration_restore_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.declaration_restore_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Declaration>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->declaration_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_declaration

> delete_declaration(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeclarationApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_declaration(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->delete_declaration: #{e}"
end
```

#### Using the delete_declaration_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_declaration_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_declaration_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->delete_declaration_with_http_info: #{e}"
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


## get_declaration

> <Declaration> get_declaration(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeclarationApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_declaration(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->get_declaration: #{e}"
end
```

#### Using the get_declaration_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Declaration>, Integer, Hash)> get_declaration_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_declaration_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Declaration>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->get_declaration_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_declarations

> <Array<Declaration>> get_declarations(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeclarationApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_declarations(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->get_declarations: #{e}"
end
```

#### Using the get_declarations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Declaration>>, Integer, Hash)> get_declarations_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_declarations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Declaration>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->get_declarations_with_http_info: #{e}"
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

[**Array&lt;Declaration&gt;**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_declaration

> <Declaration> update_declaration(id, declaration_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeclarationApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
declaration_update = SimplebillyApi::DeclarationUpdate.new # DeclarationUpdate | 

begin
  
  result = api_instance.update_declaration(id, declaration_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->update_declaration: #{e}"
end
```

#### Using the update_declaration_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Declaration>, Integer, Hash)> update_declaration_with_http_info(id, declaration_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_declaration_with_http_info(id, declaration_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Declaration>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeclarationApi->update_declaration_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **declaration_update** | [**DeclarationUpdate**](DeclarationUpdate.md) |  |  |

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

