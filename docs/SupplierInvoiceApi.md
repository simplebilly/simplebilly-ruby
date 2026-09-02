# SimplebillyApi::SupplierInvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_supplier_invoice**](SupplierInvoiceApi.md#create_supplier_invoice) | **POST** /api/v1/supplier-invoices |  |
| [**delete_supplier_invoice**](SupplierInvoiceApi.md#delete_supplier_invoice) | **DELETE** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**get_supplier_invoice**](SupplierInvoiceApi.md#get_supplier_invoice) | **GET** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**list_supplier_invoices**](SupplierInvoiceApi.md#list_supplier_invoices) | **GET** /api/v1/supplier-invoices/ |  |
| [**update_supplier_invoice**](SupplierInvoiceApi.md#update_supplier_invoice) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**update_supplier_invoice_status**](SupplierInvoiceApi.md#update_supplier_invoice_status) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id}/status |  |


## create_supplier_invoice

> <SupplierInvoice> create_supplier_invoice(supplier_invoice)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierInvoiceApi.new
supplier_invoice = SimplebillyApi::SupplierInvoice.new({invoice_date: Date.today, invoice_number: 'invoice_number_example', line_items: 3.56, status: SimplebillyApi::SupplierInvoiceStatus::DRAFT}) # SupplierInvoice | 

begin
  
  result = api_instance.create_supplier_invoice(supplier_invoice)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->create_supplier_invoice: #{e}"
end
```

#### Using the create_supplier_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupplierInvoice>, Integer, Hash)> create_supplier_invoice_with_http_info(supplier_invoice)

```ruby
begin
  
  data, status_code, headers = api_instance.create_supplier_invoice_with_http_info(supplier_invoice)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupplierInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->create_supplier_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_invoice** | [**SupplierInvoice**](SupplierInvoice.md) |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_supplier_invoice

> delete_supplier_invoice(supplier_invoice_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierInvoiceApi.new
supplier_invoice_id = 'supplier_invoice_id_example' # String | 

begin
  
  api_instance.delete_supplier_invoice(supplier_invoice_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->delete_supplier_invoice: #{e}"
end
```

#### Using the delete_supplier_invoice_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_supplier_invoice_with_http_info(supplier_invoice_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_supplier_invoice_with_http_info(supplier_invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->delete_supplier_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_invoice_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_supplier_invoice

> <SupplierInvoice> get_supplier_invoice(supplier_invoice_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierInvoiceApi.new
supplier_invoice_id = 'supplier_invoice_id_example' # String | 

begin
  
  result = api_instance.get_supplier_invoice(supplier_invoice_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->get_supplier_invoice: #{e}"
end
```

#### Using the get_supplier_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupplierInvoice>, Integer, Hash)> get_supplier_invoice_with_http_info(supplier_invoice_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_supplier_invoice_with_http_info(supplier_invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupplierInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->get_supplier_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_invoice_id** | **String** |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_supplier_invoices

> <Array<SupplierInvoice>> list_supplier_invoices(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierInvoiceApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  purchase_order_id: 'purchase_order_id_example', # String | 
  supplier_name: 'supplier_name_example' # String | 
}

begin
  
  result = api_instance.list_supplier_invoices(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->list_supplier_invoices: #{e}"
end
```

#### Using the list_supplier_invoices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<SupplierInvoice>>, Integer, Hash)> list_supplier_invoices_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_supplier_invoices_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<SupplierInvoice>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->list_supplier_invoices_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **purchase_order_id** | **String** |  | [optional] |
| **supplier_name** | **String** |  | [optional] |

### Return type

[**Array&lt;SupplierInvoice&gt;**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_supplier_invoice

> <SupplierInvoice> update_supplier_invoice(supplier_invoice_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierInvoiceApi.new
supplier_invoice_id = 'supplier_invoice_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_supplier_invoice(supplier_invoice_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->update_supplier_invoice: #{e}"
end
```

#### Using the update_supplier_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupplierInvoice>, Integer, Hash)> update_supplier_invoice_with_http_info(supplier_invoice_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_supplier_invoice_with_http_info(supplier_invoice_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupplierInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->update_supplier_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_invoice_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_supplier_invoice_status

> <SupplierInvoice> update_supplier_invoice_status(supplier_invoice_id, supplier_invoice_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierInvoiceApi.new
supplier_invoice_id = 'supplier_invoice_id_example' # String | 
supplier_invoice_status_update = SimplebillyApi::SupplierInvoiceStatusUpdate.new({status: 'status_example'}) # SupplierInvoiceStatusUpdate | 

begin
  
  result = api_instance.update_supplier_invoice_status(supplier_invoice_id, supplier_invoice_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->update_supplier_invoice_status: #{e}"
end
```

#### Using the update_supplier_invoice_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupplierInvoice>, Integer, Hash)> update_supplier_invoice_status_with_http_info(supplier_invoice_id, supplier_invoice_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_supplier_invoice_status_with_http_info(supplier_invoice_id, supplier_invoice_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupplierInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierInvoiceApi->update_supplier_invoice_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_invoice_id** | **String** |  |  |
| **supplier_invoice_status_update** | [**SupplierInvoiceStatusUpdate**](SupplierInvoiceStatusUpdate.md) |  |  |

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

