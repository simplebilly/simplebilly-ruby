# SimplebillyApi::WarehouseApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_warehouse**](WarehouseApi.md#create_warehouse) | **POST** /api/v1/warehouses |  |
| [**delete_warehouse**](WarehouseApi.md#delete_warehouse) | **DELETE** /api/v1/warehouses/{warehouse_id} |  |
| [**get_warehouse**](WarehouseApi.md#get_warehouse) | **GET** /api/v1/warehouses/{warehouse_id} |  |
| [**list_warehouses**](WarehouseApi.md#list_warehouses) | **GET** /api/v1/warehouses/ |  |
| [**update_warehouse**](WarehouseApi.md#update_warehouse) | **PUT** /api/v1/warehouses/{warehouse_id} |  |


## create_warehouse

> <Warehouse> create_warehouse(warehouse)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseApi.new
warehouse = SimplebillyApi::Warehouse.new({code: 'code_example', name: 'name_example'}) # Warehouse | 

begin
  
  result = api_instance.create_warehouse(warehouse)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->create_warehouse: #{e}"
end
```

#### Using the create_warehouse_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Warehouse>, Integer, Hash)> create_warehouse_with_http_info(warehouse)

```ruby
begin
  
  data, status_code, headers = api_instance.create_warehouse_with_http_info(warehouse)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Warehouse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->create_warehouse_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse** | [**Warehouse**](Warehouse.md) |  |  |

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_warehouse

> delete_warehouse(warehouse_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseApi.new
warehouse_id = 'warehouse_id_example' # String | 

begin
  
  api_instance.delete_warehouse(warehouse_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->delete_warehouse: #{e}"
end
```

#### Using the delete_warehouse_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_warehouse_with_http_info(warehouse_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_warehouse_with_http_info(warehouse_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->delete_warehouse_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_warehouse

> <Warehouse> get_warehouse(warehouse_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseApi.new
warehouse_id = 'warehouse_id_example' # String | 

begin
  
  result = api_instance.get_warehouse(warehouse_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->get_warehouse: #{e}"
end
```

#### Using the get_warehouse_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Warehouse>, Integer, Hash)> get_warehouse_with_http_info(warehouse_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_warehouse_with_http_info(warehouse_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Warehouse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->get_warehouse_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse_id** | **String** |  |  |

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_warehouses

> <Array<Warehouse>> list_warehouses(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  is_active: true # Boolean | 
}

begin
  
  result = api_instance.list_warehouses(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->list_warehouses: #{e}"
end
```

#### Using the list_warehouses_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Warehouse>>, Integer, Hash)> list_warehouses_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_warehouses_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Warehouse>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->list_warehouses_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |

### Return type

[**Array&lt;Warehouse&gt;**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_warehouse

> <Warehouse> update_warehouse(warehouse_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseApi.new
warehouse_id = 'warehouse_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_warehouse(warehouse_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->update_warehouse: #{e}"
end
```

#### Using the update_warehouse_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Warehouse>, Integer, Hash)> update_warehouse_with_http_info(warehouse_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_warehouse_with_http_info(warehouse_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Warehouse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseApi->update_warehouse_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

