# SimplebillyApi::ShareholderApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_shareholder**](ShareholderApi.md#create_shareholder) | **POST** /api/v1/shareholders |  |
| [**delete_shareholder**](ShareholderApi.md#delete_shareholder) | **DELETE** /api/v1/shareholders/{id} |  |
| [**get_shareholder**](ShareholderApi.md#get_shareholder) | **GET** /api/v1/shareholders/{id} |  |
| [**get_shareholders**](ShareholderApi.md#get_shareholders) | **GET** /api/v1/shareholders/ |  |
| [**update_shareholder**](ShareholderApi.md#update_shareholder) | **PUT** /api/v1/shareholders/{id} |  |


## create_shareholder

> <Shareholder> create_shareholder(shareholder_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShareholderApi.new
shareholder_create = SimplebillyApi::ShareholderCreate.new # ShareholderCreate | 

begin
  
  result = api_instance.create_shareholder(shareholder_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->create_shareholder: #{e}"
end
```

#### Using the create_shareholder_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Shareholder>, Integer, Hash)> create_shareholder_with_http_info(shareholder_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_shareholder_with_http_info(shareholder_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Shareholder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->create_shareholder_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shareholder_create** | [**ShareholderCreate**](ShareholderCreate.md) |  |  |

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_shareholder

> delete_shareholder(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShareholderApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_shareholder(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->delete_shareholder: #{e}"
end
```

#### Using the delete_shareholder_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_shareholder_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_shareholder_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->delete_shareholder_with_http_info: #{e}"
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


## get_shareholder

> <Shareholder> get_shareholder(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShareholderApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_shareholder(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->get_shareholder: #{e}"
end
```

#### Using the get_shareholder_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Shareholder>, Integer, Hash)> get_shareholder_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_shareholder_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Shareholder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->get_shareholder_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_shareholders

> <Array<Shareholder>> get_shareholders(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShareholderApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_shareholders(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->get_shareholders: #{e}"
end
```

#### Using the get_shareholders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Shareholder>>, Integer, Hash)> get_shareholders_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_shareholders_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Shareholder>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->get_shareholders_with_http_info: #{e}"
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

[**Array&lt;Shareholder&gt;**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_shareholder

> <Shareholder> update_shareholder(id, shareholder_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShareholderApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
shareholder_update = SimplebillyApi::ShareholderUpdate.new # ShareholderUpdate | 

begin
  
  result = api_instance.update_shareholder(id, shareholder_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->update_shareholder: #{e}"
end
```

#### Using the update_shareholder_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Shareholder>, Integer, Hash)> update_shareholder_with_http_info(id, shareholder_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_shareholder_with_http_info(id, shareholder_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Shareholder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShareholderApi->update_shareholder_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **shareholder_update** | [**ShareholderUpdate**](ShareholderUpdate.md) |  |  |

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

