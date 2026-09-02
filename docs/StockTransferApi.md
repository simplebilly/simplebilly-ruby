# SimplebillyApi::StockTransferApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_stock_transfer**](StockTransferApi.md#create_stock_transfer) | **POST** /api/v1/stock-transfers |  |
| [**delete_stock_transfer**](StockTransferApi.md#delete_stock_transfer) | **DELETE** /api/v1/stock-transfers/{stock_transfer_id} |  |
| [**get_stock_transfer**](StockTransferApi.md#get_stock_transfer) | **GET** /api/v1/stock-transfers/{stock_transfer_id} |  |
| [**list_stock_transfers**](StockTransferApi.md#list_stock_transfers) | **GET** /api/v1/stock-transfers/ |  |
| [**update_stock_transfer_status**](StockTransferApi.md#update_stock_transfer_status) | **PUT** /api/v1/stock-transfers/{stock_transfer_id}/status |  |


## create_stock_transfer

> <StockTransfer> create_stock_transfer(stock_transfer)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StockTransferApi.new
stock_transfer = SimplebillyApi::StockTransfer.new({line_items: 3.56, source_warehouse_id: 'source_warehouse_id_example', status: SimplebillyApi::StockTransferStatus::DRAFT, target_warehouse_id: 'target_warehouse_id_example', transfer_date: Date.today, transfer_number: 'transfer_number_example'}) # StockTransfer | 

begin
  
  result = api_instance.create_stock_transfer(stock_transfer)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->create_stock_transfer: #{e}"
end
```

#### Using the create_stock_transfer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StockTransfer>, Integer, Hash)> create_stock_transfer_with_http_info(stock_transfer)

```ruby
begin
  
  data, status_code, headers = api_instance.create_stock_transfer_with_http_info(stock_transfer)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StockTransfer>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->create_stock_transfer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stock_transfer** | [**StockTransfer**](StockTransfer.md) |  |  |

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_stock_transfer

> delete_stock_transfer(stock_transfer_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StockTransferApi.new
stock_transfer_id = 'stock_transfer_id_example' # String | 

begin
  
  api_instance.delete_stock_transfer(stock_transfer_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->delete_stock_transfer: #{e}"
end
```

#### Using the delete_stock_transfer_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_stock_transfer_with_http_info(stock_transfer_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_stock_transfer_with_http_info(stock_transfer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->delete_stock_transfer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stock_transfer_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_stock_transfer

> <StockTransfer> get_stock_transfer(stock_transfer_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StockTransferApi.new
stock_transfer_id = 'stock_transfer_id_example' # String | 

begin
  
  result = api_instance.get_stock_transfer(stock_transfer_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->get_stock_transfer: #{e}"
end
```

#### Using the get_stock_transfer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StockTransfer>, Integer, Hash)> get_stock_transfer_with_http_info(stock_transfer_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_stock_transfer_with_http_info(stock_transfer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StockTransfer>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->get_stock_transfer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stock_transfer_id** | **String** |  |  |

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_stock_transfers

> <Array<StockTransfer>> list_stock_transfers(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StockTransferApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  warehouse_id: 'warehouse_id_example' # String | 
}

begin
  
  result = api_instance.list_stock_transfers(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->list_stock_transfers: #{e}"
end
```

#### Using the list_stock_transfers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<StockTransfer>>, Integer, Hash)> list_stock_transfers_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_stock_transfers_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<StockTransfer>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->list_stock_transfers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **warehouse_id** | **String** |  | [optional] |

### Return type

[**Array&lt;StockTransfer&gt;**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_stock_transfer_status

> <StockTransfer> update_stock_transfer_status(stock_transfer_id, stock_transfer_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::StockTransferApi.new
stock_transfer_id = 'stock_transfer_id_example' # String | 
stock_transfer_status_update = SimplebillyApi::StockTransferStatusUpdate.new({status: 'status_example'}) # StockTransferStatusUpdate | 

begin
  
  result = api_instance.update_stock_transfer_status(stock_transfer_id, stock_transfer_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->update_stock_transfer_status: #{e}"
end
```

#### Using the update_stock_transfer_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StockTransfer>, Integer, Hash)> update_stock_transfer_status_with_http_info(stock_transfer_id, stock_transfer_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_stock_transfer_status_with_http_info(stock_transfer_id, stock_transfer_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StockTransfer>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling StockTransferApi->update_stock_transfer_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stock_transfer_id** | **String** |  |  |
| **stock_transfer_status_update** | [**StockTransferStatusUpdate**](StockTransferStatusUpdate.md) |  |  |

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

