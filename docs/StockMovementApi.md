# SimplebillyApi::StockMovementApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_stock_movement**](StockMovementApi.md#get_stock_movement) | **GET** /api/v1/stock-movements/{movement_id} |  |
| [**list_stock_movements**](StockMovementApi.md#list_stock_movements) | **GET** /api/v1/stock-movements/ |  |


## get_stock_movement

> <StockMovement> get_stock_movement(movement_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StockMovementApi.new
movement_id = 'movement_id_example' # String | 

begin
  
  result = api_instance.get_stock_movement(movement_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockMovementApi->get_stock_movement: #{e}"
end
```

#### Using the get_stock_movement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StockMovement>, Integer, Hash)> get_stock_movement_with_http_info(movement_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_stock_movement_with_http_info(movement_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StockMovement>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockMovementApi->get_stock_movement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **movement_id** | **String** |  |  |

### Return type

[**StockMovement**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_stock_movements

> <Array<StockMovement>> list_stock_movements(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StockMovementApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  product_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  warehouse_id: 'warehouse_id_example', # String | 
  movement_type: 'movement_type_example', # String | 
  from: Date.parse('2013-10-20'), # Date | Only movements on or after this date (inclusive).
  to: Date.parse('2013-10-20') # Date | Only movements on or before this date (inclusive).
}

begin
  
  result = api_instance.list_stock_movements(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockMovementApi->list_stock_movements: #{e}"
end
```

#### Using the list_stock_movements_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<StockMovement>>, Integer, Hash)> list_stock_movements_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_stock_movements_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<StockMovement>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockMovementApi->list_stock_movements_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **warehouse_id** | **String** |  | [optional] |
| **movement_type** | **String** |  | [optional] |
| **from** | **Date** | Only movements on or after this date (inclusive). | [optional] |
| **to** | **Date** | Only movements on or before this date (inclusive). | [optional] |

### Return type

[**Array&lt;StockMovement&gt;**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

