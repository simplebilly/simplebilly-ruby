# SimplebillyApi::PurchaseOrderApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_purchase_order**](PurchaseOrderApi.md#create_purchase_order) | **POST** /api/v1/purchase-orders |  |
| [**delete_purchase_order**](PurchaseOrderApi.md#delete_purchase_order) | **DELETE** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**get_purchase_order**](PurchaseOrderApi.md#get_purchase_order) | **GET** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**list_purchase_orders**](PurchaseOrderApi.md#list_purchase_orders) | **GET** /api/v1/purchase-orders/ |  |
| [**match_invoice**](PurchaseOrderApi.md#match_invoice) | **POST** /api/v1/purchase-orders/{purchase_order_id}/match-invoice | 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product. |
| [**update_purchase_order**](PurchaseOrderApi.md#update_purchase_order) | **PUT** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**update_purchase_order_status**](PurchaseOrderApi.md#update_purchase_order_status) | **PUT** /api/v1/purchase-orders/{purchase_order_id}/status |  |


## create_purchase_order

> <PurchaseOrder> create_purchase_order(purchase_order)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PurchaseOrderApi.new
purchase_order = SimplebillyApi::PurchaseOrder.new({order_date: Date.today, po_number: 'po_number_example', status: SimplebillyApi::PurchaseOrderStatus::DRAFT}) # PurchaseOrder | 

begin
  
  result = api_instance.create_purchase_order(purchase_order)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->create_purchase_order: #{e}"
end
```

#### Using the create_purchase_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PurchaseOrder>, Integer, Hash)> create_purchase_order_with_http_info(purchase_order)

```ruby
begin
  
  data, status_code, headers = api_instance.create_purchase_order_with_http_info(purchase_order)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PurchaseOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->create_purchase_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **purchase_order** | [**PurchaseOrder**](PurchaseOrder.md) |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_purchase_order

> delete_purchase_order(purchase_order_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PurchaseOrderApi.new
purchase_order_id = 'purchase_order_id_example' # String | 

begin
  
  api_instance.delete_purchase_order(purchase_order_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->delete_purchase_order: #{e}"
end
```

#### Using the delete_purchase_order_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_purchase_order_with_http_info(purchase_order_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_purchase_order_with_http_info(purchase_order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->delete_purchase_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **purchase_order_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_purchase_order

> <PurchaseOrder> get_purchase_order(purchase_order_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PurchaseOrderApi.new
purchase_order_id = 'purchase_order_id_example' # String | 

begin
  
  result = api_instance.get_purchase_order(purchase_order_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->get_purchase_order: #{e}"
end
```

#### Using the get_purchase_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PurchaseOrder>, Integer, Hash)> get_purchase_order_with_http_info(purchase_order_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_purchase_order_with_http_info(purchase_order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PurchaseOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->get_purchase_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **purchase_order_id** | **String** |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_purchase_orders

> <Array<PurchaseOrder>> list_purchase_orders(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PurchaseOrderApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  supplier_name: 'supplier_name_example', # String | 
  search: 'search_example' # String | 
}

begin
  
  result = api_instance.list_purchase_orders(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->list_purchase_orders: #{e}"
end
```

#### Using the list_purchase_orders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PurchaseOrder>>, Integer, Hash)> list_purchase_orders_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_purchase_orders_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PurchaseOrder>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->list_purchase_orders_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **supplier_name** | **String** |  | [optional] |
| **search** | **String** |  | [optional] |

### Return type

[**Array&lt;PurchaseOrder&gt;**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## match_invoice

> Object match_invoice(purchase_order_id, invoice_match_request)

3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PurchaseOrderApi.new
purchase_order_id = 'purchase_order_id_example' # String | 
invoice_match_request = SimplebillyApi::InvoiceMatchRequest.new({supplier_invoice_id: 'supplier_invoice_id_example'}) # InvoiceMatchRequest | 

begin
  # 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
  result = api_instance.match_invoice(purchase_order_id, invoice_match_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->match_invoice: #{e}"
end
```

#### Using the match_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> match_invoice_with_http_info(purchase_order_id, invoice_match_request)

```ruby
begin
  # 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
  data, status_code, headers = api_instance.match_invoice_with_http_info(purchase_order_id, invoice_match_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->match_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **purchase_order_id** | **String** |  |  |
| **invoice_match_request** | [**InvoiceMatchRequest**](InvoiceMatchRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_purchase_order

> <PurchaseOrder> update_purchase_order(purchase_order_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PurchaseOrderApi.new
purchase_order_id = 'purchase_order_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_purchase_order(purchase_order_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->update_purchase_order: #{e}"
end
```

#### Using the update_purchase_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PurchaseOrder>, Integer, Hash)> update_purchase_order_with_http_info(purchase_order_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_purchase_order_with_http_info(purchase_order_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PurchaseOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->update_purchase_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **purchase_order_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_purchase_order_status

> <PurchaseOrder> update_purchase_order_status(purchase_order_id, purchase_order_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PurchaseOrderApi.new
purchase_order_id = 'purchase_order_id_example' # String | 
purchase_order_status_update = SimplebillyApi::PurchaseOrderStatusUpdate.new({status: 'status_example'}) # PurchaseOrderStatusUpdate | 

begin
  
  result = api_instance.update_purchase_order_status(purchase_order_id, purchase_order_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->update_purchase_order_status: #{e}"
end
```

#### Using the update_purchase_order_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PurchaseOrder>, Integer, Hash)> update_purchase_order_status_with_http_info(purchase_order_id, purchase_order_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_purchase_order_status_with_http_info(purchase_order_id, purchase_order_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PurchaseOrder>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PurchaseOrderApi->update_purchase_order_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **purchase_order_id** | **String** |  |  |
| **purchase_order_status_update** | [**PurchaseOrderStatusUpdate**](PurchaseOrderStatusUpdate.md) |  |  |

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

