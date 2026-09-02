# SimplebillyApi::WarehouseStockApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_warehouse_stock**](WarehouseStockApi.md#create_warehouse_stock) | **POST** /api/v1/warehouses/{warehouse_id}/stock |  |
| [**delete_warehouse_stock**](WarehouseStockApi.md#delete_warehouse_stock) | **DELETE** /api/v1/warehouses/{warehouse_id}/stock/{product_id} |  |
| [**list_warehouse_stock**](WarehouseStockApi.md#list_warehouse_stock) | **GET** /api/v1/warehouses/{warehouse_id}/stock |  |
| [**update_warehouse_stock**](WarehouseStockApi.md#update_warehouse_stock) | **PUT** /api/v1/warehouses/{warehouse_id}/stock/{product_id} |  |


## create_warehouse_stock

> <WarehouseStock> create_warehouse_stock(warehouse_id, stock_adjustment)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseStockApi.new
warehouse_id = 'warehouse_id_example' # String | 
stock_adjustment = SimplebillyApi::StockAdjustment.new({quantity: 3.56}) # StockAdjustment | 

begin
  
  result = api_instance.create_warehouse_stock(warehouse_id, stock_adjustment)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->create_warehouse_stock: #{e}"
end
```

#### Using the create_warehouse_stock_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WarehouseStock>, Integer, Hash)> create_warehouse_stock_with_http_info(warehouse_id, stock_adjustment)

```ruby
begin
  
  data, status_code, headers = api_instance.create_warehouse_stock_with_http_info(warehouse_id, stock_adjustment)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WarehouseStock>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->create_warehouse_stock_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse_id** | **String** |  |  |
| **stock_adjustment** | [**StockAdjustment**](StockAdjustment.md) |  |  |

### Return type

[**WarehouseStock**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_warehouse_stock

> delete_warehouse_stock(warehouse_id, product_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseStockApi.new
warehouse_id = 'warehouse_id_example' # String | 
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_warehouse_stock(warehouse_id, product_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->delete_warehouse_stock: #{e}"
end
```

#### Using the delete_warehouse_stock_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_warehouse_stock_with_http_info(warehouse_id, product_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_warehouse_stock_with_http_info(warehouse_id, product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->delete_warehouse_stock_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse_id** | **String** |  |  |
| **product_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_warehouse_stock

> <Array<WarehouseStock>> list_warehouse_stock(warehouse_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseStockApi.new
warehouse_id = 'warehouse_id_example' # String | 

begin
  
  result = api_instance.list_warehouse_stock(warehouse_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->list_warehouse_stock: #{e}"
end
```

#### Using the list_warehouse_stock_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<WarehouseStock>>, Integer, Hash)> list_warehouse_stock_with_http_info(warehouse_id)

```ruby
begin
  
  data, status_code, headers = api_instance.list_warehouse_stock_with_http_info(warehouse_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<WarehouseStock>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->list_warehouse_stock_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse_id** | **String** |  |  |

### Return type

[**Array&lt;WarehouseStock&gt;**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_warehouse_stock

> <WarehouseStock> update_warehouse_stock(warehouse_id, product_id, stock_adjustment)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WarehouseStockApi.new
warehouse_id = 'warehouse_id_example' # String | 
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
stock_adjustment = SimplebillyApi::StockAdjustment.new({quantity: 3.56}) # StockAdjustment | 

begin
  
  result = api_instance.update_warehouse_stock(warehouse_id, product_id, stock_adjustment)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->update_warehouse_stock: #{e}"
end
```

#### Using the update_warehouse_stock_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WarehouseStock>, Integer, Hash)> update_warehouse_stock_with_http_info(warehouse_id, product_id, stock_adjustment)

```ruby
begin
  
  data, status_code, headers = api_instance.update_warehouse_stock_with_http_info(warehouse_id, product_id, stock_adjustment)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WarehouseStock>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WarehouseStockApi->update_warehouse_stock_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warehouse_id** | **String** |  |  |
| **product_id** | **String** |  |  |
| **stock_adjustment** | [**StockAdjustment**](StockAdjustment.md) |  |  |

### Return type

[**WarehouseStock**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

