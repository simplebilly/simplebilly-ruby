# SimplebillyApi::QuotationApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_quotation**](QuotationApi.md#create_quotation) | **POST** /api/v1/quotations |  |
| [**delete_quotation**](QuotationApi.md#delete_quotation) | **DELETE** /api/v1/quotations/{quotation_id} |  |
| [**download_quotation_pdf**](QuotationApi.md#download_quotation_pdf) | **GET** /api/v1/quotations/{quotation_id}/pdf |  |
| [**get_quotation**](QuotationApi.md#get_quotation) | **GET** /api/v1/quotations/{quotation_id} |  |
| [**list_quotations**](QuotationApi.md#list_quotations) | **GET** /api/v1/quotations/ |  |
| [**pursue_quotation**](QuotationApi.md#pursue_quotation) | **POST** /api/v1/quotations/{quotation_id}/pursue |  |
| [**quotation_restore**](QuotationApi.md#quotation_restore) | **POST** /api/v1/quotations/{quotation_id}/restore |  |
| [**update_quotation**](QuotationApi.md#update_quotation) | **PUT** /api/v1/quotations/{quotation_id} |  |


## create_quotation

> <Quotation> create_quotation(quotation_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
quotation_create = SimplebillyApi::QuotationCreate.new({currency: 'currency_example', voucher_date: Date.today, voucher_status: SimplebillyApi::VoucherStatus::OPEN}) # QuotationCreate | 

begin
  
  result = api_instance.create_quotation(quotation_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->create_quotation: #{e}"
end
```

#### Using the create_quotation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Quotation>, Integer, Hash)> create_quotation_with_http_info(quotation_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_quotation_with_http_info(quotation_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Quotation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->create_quotation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quotation_create** | [**QuotationCreate**](QuotationCreate.md) |  |  |

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_quotation

> delete_quotation(quotation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
quotation_id = 'quotation_id_example' # String | 

begin
  
  api_instance.delete_quotation(quotation_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->delete_quotation: #{e}"
end
```

#### Using the delete_quotation_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_quotation_with_http_info(quotation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_quotation_with_http_info(quotation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->delete_quotation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quotation_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_quotation_pdf

> download_quotation_pdf(quotation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
quotation_id = 'quotation_id_example' # String | 

begin
  
  api_instance.download_quotation_pdf(quotation_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->download_quotation_pdf: #{e}"
end
```

#### Using the download_quotation_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> download_quotation_pdf_with_http_info(quotation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.download_quotation_pdf_with_http_info(quotation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->download_quotation_pdf_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quotation_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json


## get_quotation

> <Quotation> get_quotation(quotation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
quotation_id = 'quotation_id_example' # String | 

begin
  
  result = api_instance.get_quotation(quotation_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->get_quotation: #{e}"
end
```

#### Using the get_quotation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Quotation>, Integer, Hash)> get_quotation_with_http_info(quotation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_quotation_with_http_info(quotation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Quotation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->get_quotation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quotation_id** | **String** |  |  |

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_quotations

> <Array<Quotation>> list_quotations(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.list_quotations(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->list_quotations: #{e}"
end
```

#### Using the list_quotations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Quotation>>, Integer, Hash)> list_quotations_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_quotations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Quotation>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->list_quotations_with_http_info: #{e}"
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

[**Array&lt;Quotation&gt;**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pursue_quotation

> <OrderConfirmation> pursue_quotation(quotation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
quotation_id = 'quotation_id_example' # String | 

begin
  
  result = api_instance.pursue_quotation(quotation_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->pursue_quotation: #{e}"
end
```

#### Using the pursue_quotation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrderConfirmation>, Integer, Hash)> pursue_quotation_with_http_info(quotation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.pursue_quotation_with_http_info(quotation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrderConfirmation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->pursue_quotation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quotation_id** | **String** |  |  |

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## quotation_restore

> <Quotation> quotation_restore(quotation_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
quotation_id = 'quotation_id_example' # String | 

begin
  
  result = api_instance.quotation_restore(quotation_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->quotation_restore: #{e}"
end
```

#### Using the quotation_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Quotation>, Integer, Hash)> quotation_restore_with_http_info(quotation_id)

```ruby
begin
  
  data, status_code, headers = api_instance.quotation_restore_with_http_info(quotation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Quotation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->quotation_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quotation_id** | **String** |  |  |

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_quotation

> <Quotation> update_quotation(quotation_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::QuotationApi.new
quotation_id = 'quotation_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_quotation(quotation_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->update_quotation: #{e}"
end
```

#### Using the update_quotation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Quotation>, Integer, Hash)> update_quotation_with_http_info(quotation_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_quotation_with_http_info(quotation_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Quotation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling QuotationApi->update_quotation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quotation_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

