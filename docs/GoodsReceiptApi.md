# SimplebillyApi::GoodsReceiptApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_goods_receipt**](GoodsReceiptApi.md#create_goods_receipt) | **POST** /api/v1/goods-receipts |  |
| [**delete_goods_receipt**](GoodsReceiptApi.md#delete_goods_receipt) | **DELETE** /api/v1/goods-receipts/{goods_receipt_id} |  |
| [**get_goods_receipt**](GoodsReceiptApi.md#get_goods_receipt) | **GET** /api/v1/goods-receipts/{goods_receipt_id} |  |
| [**list_goods_receipts**](GoodsReceiptApi.md#list_goods_receipts) | **GET** /api/v1/goods-receipts/ |  |


## create_goods_receipt

> <GoodsReceipt> create_goods_receipt(goods_receipt)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GoodsReceiptApi.new
goods_receipt = SimplebillyApi::GoodsReceipt.new({gr_number: 'gr_number_example', line_items: 3.56, receipt_date: Date.today, warehouse_id: 'warehouse_id_example'}) # GoodsReceipt | 

begin
  
  result = api_instance.create_goods_receipt(goods_receipt)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->create_goods_receipt: #{e}"
end
```

#### Using the create_goods_receipt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GoodsReceipt>, Integer, Hash)> create_goods_receipt_with_http_info(goods_receipt)

```ruby
begin
  
  data, status_code, headers = api_instance.create_goods_receipt_with_http_info(goods_receipt)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GoodsReceipt>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->create_goods_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **goods_receipt** | [**GoodsReceipt**](GoodsReceipt.md) |  |  |

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_goods_receipt

> delete_goods_receipt(goods_receipt_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GoodsReceiptApi.new
goods_receipt_id = 'goods_receipt_id_example' # String | 

begin
  
  api_instance.delete_goods_receipt(goods_receipt_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->delete_goods_receipt: #{e}"
end
```

#### Using the delete_goods_receipt_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_goods_receipt_with_http_info(goods_receipt_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_goods_receipt_with_http_info(goods_receipt_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->delete_goods_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **goods_receipt_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_goods_receipt

> <GoodsReceipt> get_goods_receipt(goods_receipt_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GoodsReceiptApi.new
goods_receipt_id = 'goods_receipt_id_example' # String | 

begin
  
  result = api_instance.get_goods_receipt(goods_receipt_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->get_goods_receipt: #{e}"
end
```

#### Using the get_goods_receipt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GoodsReceipt>, Integer, Hash)> get_goods_receipt_with_http_info(goods_receipt_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_goods_receipt_with_http_info(goods_receipt_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GoodsReceipt>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->get_goods_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **goods_receipt_id** | **String** |  |  |

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_goods_receipts

> <Array<GoodsReceipt>> list_goods_receipts(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GoodsReceiptApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  purchase_order_id: 'purchase_order_id_example', # String | 
  supplier_name: 'supplier_name_example', # String | 
  warehouse_id: 'warehouse_id_example' # String | 
}

begin
  
  result = api_instance.list_goods_receipts(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->list_goods_receipts: #{e}"
end
```

#### Using the list_goods_receipts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<GoodsReceipt>>, Integer, Hash)> list_goods_receipts_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_goods_receipts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<GoodsReceipt>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GoodsReceiptApi->list_goods_receipts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **purchase_order_id** | **String** |  | [optional] |
| **supplier_name** | **String** |  | [optional] |
| **warehouse_id** | **String** |  | [optional] |

### Return type

[**Array&lt;GoodsReceipt&gt;**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

