# SimplebillyApi::DownPaymentInvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**download_down_payment_invoice_pdf**](DownPaymentInvoiceApi.md#download_down_payment_invoice_pdf) | **GET** /api/v1/down-payment-invoices/{id}/pdf |  |
| [**get_down_payment_invoice**](DownPaymentInvoiceApi.md#get_down_payment_invoice) | **GET** /api/v1/down-payment-invoices/{id} |  |
| [**list_down_payment_invoices**](DownPaymentInvoiceApi.md#list_down_payment_invoices) | **GET** /api/v1/down-payment-invoices/ |  |


## download_down_payment_invoice_pdf

> download_down_payment_invoice_pdf(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DownPaymentInvoiceApi.new
id = 'id_example' # String | 

begin
  
  api_instance.download_down_payment_invoice_pdf(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DownPaymentInvoiceApi->download_down_payment_invoice_pdf: #{e}"
end
```

#### Using the download_down_payment_invoice_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> download_down_payment_invoice_pdf_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.download_down_payment_invoice_pdf_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DownPaymentInvoiceApi->download_down_payment_invoice_pdf_with_http_info: #{e}"
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


## get_down_payment_invoice

> <DownPaymentInvoice> get_down_payment_invoice(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DownPaymentInvoiceApi.new
id = 'id_example' # String | 

begin
  
  result = api_instance.get_down_payment_invoice(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DownPaymentInvoiceApi->get_down_payment_invoice: #{e}"
end
```

#### Using the get_down_payment_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownPaymentInvoice>, Integer, Hash)> get_down_payment_invoice_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_down_payment_invoice_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownPaymentInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DownPaymentInvoiceApi->get_down_payment_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**DownPaymentInvoice**](DownPaymentInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_down_payment_invoices

> <Array<DownPaymentInvoice>> list_down_payment_invoices(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DownPaymentInvoiceApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.list_down_payment_invoices(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DownPaymentInvoiceApi->list_down_payment_invoices: #{e}"
end
```

#### Using the list_down_payment_invoices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<DownPaymentInvoice>>, Integer, Hash)> list_down_payment_invoices_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_down_payment_invoices_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<DownPaymentInvoice>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DownPaymentInvoiceApi->list_down_payment_invoices_with_http_info: #{e}"
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

[**Array&lt;DownPaymentInvoice&gt;**](DownPaymentInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

