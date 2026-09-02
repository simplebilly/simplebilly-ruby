# SimplebillyApi::ReturnOrderApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_return_order**](ReturnOrderApi.md#create_return_order) | **POST** /api/v1/returns |  |
| [**delete_return_order**](ReturnOrderApi.md#delete_return_order) | **DELETE** /api/v1/returns/{return_order_id} |  |
| [**get_return_order**](ReturnOrderApi.md#get_return_order) | **GET** /api/v1/returns/{return_order_id} |  |
| [**list_return_orders**](ReturnOrderApi.md#list_return_orders) | **GET** /api/v1/returns/ |  |
| [**return_logistics_queue**](ReturnOrderApi.md#return_logistics_queue) | **GET** /api/v1/returns/logistics-queue |  |
| [**return_logistics_summary**](ReturnOrderApi.md#return_logistics_summary) | **GET** /api/v1/returns/logistics-summary | Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse. |
| [**update_return_order**](ReturnOrderApi.md#update_return_order) | **PUT** /api/v1/returns/{return_order_id} |  |
| [**update_return_order_status**](ReturnOrderApi.md#update_return_order_status) | **PUT** /api/v1/returns/{return_order_id}/status |  |


## create_return_order

> <ReturnOrder> create_return_order(return_order)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new
return_order = SimplebillyApi::ReturnOrder.new({return_number: 'return_number_example', status: SimplebillyApi::ReturnOrderStatus::REQUESTED}) # ReturnOrder | 

begin
  
  result = api_instance.create_return_order(return_order)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->create_return_order: #{e}"
end
```

#### Using the create_return_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReturnOrder>, Integer, Hash)> create_return_order_with_http_info(return_order)

```ruby
begin
  
  data, status_code, headers = api_instance.create_return_order_with_http_info(return_order)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReturnOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->create_return_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **return_order** | [**ReturnOrder**](ReturnOrder.md) |  |  |

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_return_order

> delete_return_order(return_order_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new
return_order_id = 'return_order_id_example' # String | 

begin
  
  api_instance.delete_return_order(return_order_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->delete_return_order: #{e}"
end
```

#### Using the delete_return_order_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_return_order_with_http_info(return_order_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_return_order_with_http_info(return_order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->delete_return_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **return_order_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_return_order

> <ReturnOrder> get_return_order(return_order_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new
return_order_id = 'return_order_id_example' # String | 

begin
  
  result = api_instance.get_return_order(return_order_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->get_return_order: #{e}"
end
```

#### Using the get_return_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReturnOrder>, Integer, Hash)> get_return_order_with_http_info(return_order_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_return_order_with_http_info(return_order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReturnOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->get_return_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **return_order_id** | **String** |  |  |

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_return_orders

> <Array<ReturnOrder>> list_return_orders(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  customer_name: 'customer_name_example', # String | 
  order_number: 'order_number_example' # String | 
}

begin
  
  result = api_instance.list_return_orders(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->list_return_orders: #{e}"
end
```

#### Using the list_return_orders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ReturnOrder>>, Integer, Hash)> list_return_orders_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_return_orders_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ReturnOrder>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->list_return_orders_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **customer_name** | **String** |  | [optional] |
| **order_number** | **String** |  | [optional] |

### Return type

[**Array&lt;ReturnOrder&gt;**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## return_logistics_queue

> <Array<ReturnLogisticsQueueItem>> return_logistics_queue



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new

begin
  
  result = api_instance.return_logistics_queue
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->return_logistics_queue: #{e}"
end
```

#### Using the return_logistics_queue_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ReturnLogisticsQueueItem>>, Integer, Hash)> return_logistics_queue_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.return_logistics_queue_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ReturnLogisticsQueueItem>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->return_logistics_queue_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;ReturnLogisticsQueueItem&gt;**](ReturnLogisticsQueueItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## return_logistics_summary

> <ReturnLogisticsSummary> return_logistics_summary

Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new

begin
  # Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
  result = api_instance.return_logistics_summary
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->return_logistics_summary: #{e}"
end
```

#### Using the return_logistics_summary_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReturnLogisticsSummary>, Integer, Hash)> return_logistics_summary_with_http_info

```ruby
begin
  # Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
  data, status_code, headers = api_instance.return_logistics_summary_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReturnLogisticsSummary>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->return_logistics_summary_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ReturnLogisticsSummary**](ReturnLogisticsSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_return_order

> <ReturnOrder> update_return_order(return_order_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new
return_order_id = 'return_order_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_return_order(return_order_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->update_return_order: #{e}"
end
```

#### Using the update_return_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReturnOrder>, Integer, Hash)> update_return_order_with_http_info(return_order_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_return_order_with_http_info(return_order_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReturnOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->update_return_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **return_order_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_return_order_status

> <ReturnOrder> update_return_order_status(return_order_id, return_order_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReturnOrderApi.new
return_order_id = 'return_order_id_example' # String | 
return_order_status_update = SimplebillyApi::ReturnOrderStatusUpdate.new({status: 'status_example'}) # ReturnOrderStatusUpdate | 

begin
  
  result = api_instance.update_return_order_status(return_order_id, return_order_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->update_return_order_status: #{e}"
end
```

#### Using the update_return_order_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReturnOrder>, Integer, Hash)> update_return_order_status_with_http_info(return_order_id, return_order_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_return_order_status_with_http_info(return_order_id, return_order_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReturnOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReturnOrderApi->update_return_order_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **return_order_id** | **String** |  |  |
| **return_order_status_update** | [**ReturnOrderStatusUpdate**](ReturnOrderStatusUpdate.md) |  |  |

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

