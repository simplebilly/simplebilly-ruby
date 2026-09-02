# SimplebillyApi::ProformaInvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**convert_proforma_to_invoice**](ProformaInvoiceApi.md#convert_proforma_to_invoice) | **POST** /api/v1/proforma-invoices/{proforma_id}/convert |  |
| [**create_proforma_invoice**](ProformaInvoiceApi.md#create_proforma_invoice) | **POST** /api/v1/proforma-invoices |  |
| [**delete_proforma_invoice**](ProformaInvoiceApi.md#delete_proforma_invoice) | **DELETE** /api/v1/proforma-invoices/{proforma_id} |  |
| [**get_proforma_invoice**](ProformaInvoiceApi.md#get_proforma_invoice) | **GET** /api/v1/proforma-invoices/{proforma_id} |  |
| [**list_proforma_invoices**](ProformaInvoiceApi.md#list_proforma_invoices) | **GET** /api/v1/proforma-invoices/ |  |
| [**update_proforma_invoice**](ProformaInvoiceApi.md#update_proforma_invoice) | **PUT** /api/v1/proforma-invoices/{proforma_id} |  |


## convert_proforma_to_invoice

> <ConvertResponse> convert_proforma_to_invoice(proforma_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProformaInvoiceApi.new
proforma_id = 'proforma_id_example' # String | 

begin
  
  result = api_instance.convert_proforma_to_invoice(proforma_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->convert_proforma_to_invoice: #{e}"
end
```

#### Using the convert_proforma_to_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConvertResponse>, Integer, Hash)> convert_proforma_to_invoice_with_http_info(proforma_id)

```ruby
begin
  
  data, status_code, headers = api_instance.convert_proforma_to_invoice_with_http_info(proforma_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConvertResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->convert_proforma_to_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **proforma_id** | **String** |  |  |

### Return type

[**ConvertResponse**](ConvertResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_proforma_invoice

> <ProformaInvoice> create_proforma_invoice(proforma_invoice)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProformaInvoiceApi.new
proforma_invoice = SimplebillyApi::ProformaInvoice.new({currency: SimplebillyApi::CurrencyCode::ADP, issue_date: Date.today, line_items: 3.56, status: SimplebillyApi::ProformaInvoiceStatus::DRAFT, subtotal: 'subtotal_example', total_amount: 'total_amount_example', total_tax: 'total_tax_example'}) # ProformaInvoice | 

begin
  
  result = api_instance.create_proforma_invoice(proforma_invoice)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->create_proforma_invoice: #{e}"
end
```

#### Using the create_proforma_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProformaInvoice>, Integer, Hash)> create_proforma_invoice_with_http_info(proforma_invoice)

```ruby
begin
  
  data, status_code, headers = api_instance.create_proforma_invoice_with_http_info(proforma_invoice)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProformaInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->create_proforma_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **proforma_invoice** | [**ProformaInvoice**](ProformaInvoice.md) |  |  |

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_proforma_invoice

> delete_proforma_invoice(proforma_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProformaInvoiceApi.new
proforma_id = 'proforma_id_example' # String | 

begin
  
  api_instance.delete_proforma_invoice(proforma_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->delete_proforma_invoice: #{e}"
end
```

#### Using the delete_proforma_invoice_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_proforma_invoice_with_http_info(proforma_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_proforma_invoice_with_http_info(proforma_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->delete_proforma_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **proforma_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_proforma_invoice

> <ProformaInvoice> get_proforma_invoice(proforma_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProformaInvoiceApi.new
proforma_id = 'proforma_id_example' # String | 

begin
  
  result = api_instance.get_proforma_invoice(proforma_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->get_proforma_invoice: #{e}"
end
```

#### Using the get_proforma_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProformaInvoice>, Integer, Hash)> get_proforma_invoice_with_http_info(proforma_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_proforma_invoice_with_http_info(proforma_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProformaInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->get_proforma_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **proforma_id** | **String** |  |  |

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_proforma_invoices

> <Array<ProformaInvoice>> list_proforma_invoices(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProformaInvoiceApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  customer_id: 'customer_id_example', # String | 
  order_number: 'order_number_example' # String | 
}

begin
  
  result = api_instance.list_proforma_invoices(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->list_proforma_invoices: #{e}"
end
```

#### Using the list_proforma_invoices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProformaInvoice>>, Integer, Hash)> list_proforma_invoices_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_proforma_invoices_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProformaInvoice>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->list_proforma_invoices_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **customer_id** | **String** |  | [optional] |
| **order_number** | **String** |  | [optional] |

### Return type

[**Array&lt;ProformaInvoice&gt;**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_proforma_invoice

> <ProformaInvoice> update_proforma_invoice(proforma_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProformaInvoiceApi.new
proforma_id = 'proforma_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_proforma_invoice(proforma_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->update_proforma_invoice: #{e}"
end
```

#### Using the update_proforma_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProformaInvoice>, Integer, Hash)> update_proforma_invoice_with_http_info(proforma_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_proforma_invoice_with_http_info(proforma_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProformaInvoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProformaInvoiceApi->update_proforma_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **proforma_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

