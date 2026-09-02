# SimplebillyApi::ProductionOrderApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_production_order**](ProductionOrderApi.md#create_production_order) | **POST** /api/v1/production-orders |  |
| [**delete_production_order**](ProductionOrderApi.md#delete_production_order) | **DELETE** /api/v1/production-orders/{production_order_id} |  |
| [**get_production_order**](ProductionOrderApi.md#get_production_order) | **GET** /api/v1/production-orders/{production_order_id} |  |
| [**list_production_orders**](ProductionOrderApi.md#list_production_orders) | **GET** /api/v1/production-orders/ |  |
| [**production_order_costing**](ProductionOrderApi.md#production_order_costing) | **GET** /api/v1/production-orders/{production_order_id}/costing | Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product&#39;s sale price. |
| [**update_production_order**](ProductionOrderApi.md#update_production_order) | **PUT** /api/v1/production-orders/{production_order_id} |  |
| [**update_production_order_status**](ProductionOrderApi.md#update_production_order_status) | **PUT** /api/v1/production-orders/{production_order_id}/status |  |


## create_production_order

> <ProductionOrder> create_production_order(production_order)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductionOrderApi.new
production_order = SimplebillyApi::ProductionOrder.new({order_number: 'order_number_example', product_id: 'product_id_example', quantity: 3.56}) # ProductionOrder | 

begin
  
  result = api_instance.create_production_order(production_order)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->create_production_order: #{e}"
end
```

#### Using the create_production_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductionOrder>, Integer, Hash)> create_production_order_with_http_info(production_order)

```ruby
begin
  
  data, status_code, headers = api_instance.create_production_order_with_http_info(production_order)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductionOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->create_production_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **production_order** | [**ProductionOrder**](ProductionOrder.md) |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_production_order

> delete_production_order(production_order_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductionOrderApi.new
production_order_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_production_order(production_order_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->delete_production_order: #{e}"
end
```

#### Using the delete_production_order_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_production_order_with_http_info(production_order_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_production_order_with_http_info(production_order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->delete_production_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **production_order_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_production_order

> <ProductionOrder> get_production_order(production_order_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductionOrderApi.new
production_order_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_production_order(production_order_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->get_production_order: #{e}"
end
```

#### Using the get_production_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductionOrder>, Integer, Hash)> get_production_order_with_http_info(production_order_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_production_order_with_http_info(production_order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductionOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->get_production_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **production_order_id** | **String** |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_production_orders

> <Array<ProductionOrder>> list_production_orders(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductionOrderApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  status: 'status_example' # String | Filter by status.
}

begin
  
  result = api_instance.list_production_orders(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->list_production_orders: #{e}"
end
```

#### Using the list_production_orders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProductionOrder>>, Integer, Hash)> list_production_orders_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_production_orders_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProductionOrder>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->list_production_orders_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **status** | **String** | Filter by status. | [optional] |

### Return type

[**Array&lt;ProductionOrder&gt;**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## production_order_costing

> <ProductionOrderCosting> production_order_costing(production_order_id)

Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductionOrderApi.new
production_order_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.
  result = api_instance.production_order_costing(production_order_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->production_order_costing: #{e}"
end
```

#### Using the production_order_costing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductionOrderCosting>, Integer, Hash)> production_order_costing_with_http_info(production_order_id)

```ruby
begin
  # Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.
  data, status_code, headers = api_instance.production_order_costing_with_http_info(production_order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductionOrderCosting>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->production_order_costing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **production_order_id** | **String** |  |  |

### Return type

[**ProductionOrderCosting**](ProductionOrderCosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_production_order

> <ProductionOrder> update_production_order(production_order_id, production_order)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductionOrderApi.new
production_order_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
production_order = SimplebillyApi::ProductionOrder.new({order_number: 'order_number_example', product_id: 'product_id_example', quantity: 3.56}) # ProductionOrder | 

begin
  
  result = api_instance.update_production_order(production_order_id, production_order)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->update_production_order: #{e}"
end
```

#### Using the update_production_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductionOrder>, Integer, Hash)> update_production_order_with_http_info(production_order_id, production_order)

```ruby
begin
  
  data, status_code, headers = api_instance.update_production_order_with_http_info(production_order_id, production_order)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductionOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->update_production_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **production_order_id** | **String** |  |  |
| **production_order** | [**ProductionOrder**](ProductionOrder.md) |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_production_order_status

> <ProductionOrder> update_production_order_status(production_order_id, production_order_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProductionOrderApi.new
production_order_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
production_order_status_update = SimplebillyApi::ProductionOrderStatusUpdate.new({status: 'status_example'}) # ProductionOrderStatusUpdate | 

begin
  
  result = api_instance.update_production_order_status(production_order_id, production_order_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->update_production_order_status: #{e}"
end
```

#### Using the update_production_order_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProductionOrder>, Integer, Hash)> update_production_order_status_with_http_info(production_order_id, production_order_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_production_order_status_with_http_info(production_order_id, production_order_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProductionOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProductionOrderApi->update_production_order_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **production_order_id** | **String** |  |  |
| **production_order_status_update** | [**ProductionOrderStatusUpdate**](ProductionOrderStatusUpdate.md) |  |  |

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

