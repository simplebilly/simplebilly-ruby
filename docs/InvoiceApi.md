# SimplebillyApi::InvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_invoice**](InvoiceApi.md#create_invoice) | **POST** /api/v1/invoices |  |
| [**delete_invoice**](InvoiceApi.md#delete_invoice) | **DELETE** /api/v1/invoices/{id} |  |
| [**download_invoice_pdf**](InvoiceApi.md#download_invoice_pdf) | **GET** /api/v1/invoices/{id}/pdf |  |
| [**get_invoice**](InvoiceApi.md#get_invoice) | **GET** /api/v1/invoices/{id} |  |
| [**get_invoice_pdf_url**](InvoiceApi.md#get_invoice_pdf_url) | **GET** /api/v1/invoices/{id}/pdf-url |  |
| [**get_invoices**](InvoiceApi.md#get_invoices) | **GET** /api/v1/invoices/ |  |
| [**invoice_restore**](InvoiceApi.md#invoice_restore) | **POST** /api/v1/invoices/{id}/restore |  |
| [**update_invoice**](InvoiceApi.md#update_invoice) | **PUT** /api/v1/invoices/{id} |  |


## create_invoice

> <Invoice> create_invoice(invoice_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
invoice_create = SimplebillyApi::InvoiceCreate.new({currency: SimplebillyApi::CurrencyCode::ADP, invoice_type: SimplebillyApi::InvoiceType::INVOICE, issue_date: Date.today, line_items: 3.56, status: SimplebillyApi::InvoiceStatus::DRAFT, subtotal: 'subtotal_example', total_amount: 'total_amount_example', total_tax: 'total_tax_example'}) # InvoiceCreate | 

begin
  
  result = api_instance.create_invoice(invoice_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->create_invoice: #{e}"
end
```

#### Using the create_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> create_invoice_with_http_info(invoice_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_invoice_with_http_info(invoice_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->create_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_create** | [**InvoiceCreate**](InvoiceCreate.md) |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_invoice

> delete_invoice(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
id = 'id_example' # String | 

begin
  
  api_instance.delete_invoice(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->delete_invoice: #{e}"
end
```

#### Using the delete_invoice_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_invoice_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_invoice_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->delete_invoice_with_http_info: #{e}"
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


## download_invoice_pdf

> download_invoice_pdf(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
id = 'id_example' # String | 

begin
  
  api_instance.download_invoice_pdf(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->download_invoice_pdf: #{e}"
end
```

#### Using the download_invoice_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> download_invoice_pdf_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.download_invoice_pdf_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->download_invoice_pdf_with_http_info: #{e}"
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
- **Accept**: application/pdf, application/json


## get_invoice

> <Invoice> get_invoice(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
id = 'id_example' # String | 

begin
  
  result = api_instance.get_invoice(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->get_invoice: #{e}"
end
```

#### Using the get_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> get_invoice_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_invoice_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->get_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_invoice_pdf_url

> <InvoicePdfUrlResponse> get_invoice_pdf_url(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
id = 'id_example' # String | 

begin
  
  result = api_instance.get_invoice_pdf_url(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->get_invoice_pdf_url: #{e}"
end
```

#### Using the get_invoice_pdf_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoicePdfUrlResponse>, Integer, Hash)> get_invoice_pdf_url_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_invoice_pdf_url_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoicePdfUrlResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->get_invoice_pdf_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**InvoicePdfUrlResponse**](InvoicePdfUrlResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_invoices

> <Array<Invoice>> get_invoices(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_invoices(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->get_invoices: #{e}"
end
```

#### Using the get_invoices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Invoice>>, Integer, Hash)> get_invoices_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_invoices_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Invoice>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->get_invoices_with_http_info: #{e}"
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

[**Array&lt;Invoice&gt;**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## invoice_restore

> <Invoice> invoice_restore(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
id = 'id_example' # String | 

begin
  
  result = api_instance.invoice_restore(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->invoice_restore: #{e}"
end
```

#### Using the invoice_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> invoice_restore_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.invoice_restore_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->invoice_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_invoice

> <Invoice> update_invoice(id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InvoiceApi.new
id = 'id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_invoice(id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->update_invoice: #{e}"
end
```

#### Using the update_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> update_invoice_with_http_info(id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_invoice_with_http_info(id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InvoiceApi->update_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

