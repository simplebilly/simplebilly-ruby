# SimplebillyApi::DeliveryNoteApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_delivery_note**](DeliveryNoteApi.md#create_delivery_note) | **POST** /api/v1/delivery-notes |  |
| [**delete_delivery_note**](DeliveryNoteApi.md#delete_delivery_note) | **DELETE** /api/v1/delivery-notes/{delivery_note_id} |  |
| [**deliverynote_restore**](DeliveryNoteApi.md#deliverynote_restore) | **POST** /api/v1/delivery-notes/{delivery_note_id}/restore |  |
| [**download_delivery_note_pdf**](DeliveryNoteApi.md#download_delivery_note_pdf) | **GET** /api/v1/delivery-notes/{delivery_note_id}/pdf |  |
| [**get_delivery_note**](DeliveryNoteApi.md#get_delivery_note) | **GET** /api/v1/delivery-notes/{delivery_note_id} |  |
| [**list_delivery_notes**](DeliveryNoteApi.md#list_delivery_notes) | **GET** /api/v1/delivery-notes/ |  |
| [**pursue_delivery_note**](DeliveryNoteApi.md#pursue_delivery_note) | **POST** /api/v1/delivery-notes/{delivery_note_id}/pursue |  |


## create_delivery_note

> <DeliveryNote> create_delivery_note(delivery_note_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryNoteApi.new
delivery_note_create = SimplebillyApi::DeliveryNoteCreate.new({currency: 'currency_example', voucher_date: Date.today, voucher_status: SimplebillyApi::VoucherStatus::OPEN}) # DeliveryNoteCreate | 

begin
  
  result = api_instance.create_delivery_note(delivery_note_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->create_delivery_note: #{e}"
end
```

#### Using the create_delivery_note_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryNote>, Integer, Hash)> create_delivery_note_with_http_info(delivery_note_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_delivery_note_with_http_info(delivery_note_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryNote>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->create_delivery_note_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_note_create** | [**DeliveryNoteCreate**](DeliveryNoteCreate.md) |  |  |

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_delivery_note

> delete_delivery_note(delivery_note_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryNoteApi.new
delivery_note_id = 'delivery_note_id_example' # String | 

begin
  
  api_instance.delete_delivery_note(delivery_note_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->delete_delivery_note: #{e}"
end
```

#### Using the delete_delivery_note_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_delivery_note_with_http_info(delivery_note_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_delivery_note_with_http_info(delivery_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->delete_delivery_note_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_note_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deliverynote_restore

> <DeliveryNote> deliverynote_restore(delivery_note_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryNoteApi.new
delivery_note_id = 'delivery_note_id_example' # String | 

begin
  
  result = api_instance.deliverynote_restore(delivery_note_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->deliverynote_restore: #{e}"
end
```

#### Using the deliverynote_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryNote>, Integer, Hash)> deliverynote_restore_with_http_info(delivery_note_id)

```ruby
begin
  
  data, status_code, headers = api_instance.deliverynote_restore_with_http_info(delivery_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryNote>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->deliverynote_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_note_id** | **String** |  |  |

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_delivery_note_pdf

> download_delivery_note_pdf(delivery_note_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryNoteApi.new
delivery_note_id = 'delivery_note_id_example' # String | 

begin
  
  api_instance.download_delivery_note_pdf(delivery_note_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->download_delivery_note_pdf: #{e}"
end
```

#### Using the download_delivery_note_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> download_delivery_note_pdf_with_http_info(delivery_note_id)

```ruby
begin
  
  data, status_code, headers = api_instance.download_delivery_note_pdf_with_http_info(delivery_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->download_delivery_note_pdf_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_note_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json


## get_delivery_note

> <DeliveryNote> get_delivery_note(delivery_note_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryNoteApi.new
delivery_note_id = 'delivery_note_id_example' # String | 

begin
  
  result = api_instance.get_delivery_note(delivery_note_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->get_delivery_note: #{e}"
end
```

#### Using the get_delivery_note_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryNote>, Integer, Hash)> get_delivery_note_with_http_info(delivery_note_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_delivery_note_with_http_info(delivery_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryNote>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->get_delivery_note_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_note_id** | **String** |  |  |

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_delivery_notes

> <Array<DeliveryNote>> list_delivery_notes(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryNoteApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.list_delivery_notes(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->list_delivery_notes: #{e}"
end
```

#### Using the list_delivery_notes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<DeliveryNote>>, Integer, Hash)> list_delivery_notes_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_delivery_notes_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<DeliveryNote>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->list_delivery_notes_with_http_info: #{e}"
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

[**Array&lt;DeliveryNote&gt;**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pursue_delivery_note

> <Invoice> pursue_delivery_note(delivery_note_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryNoteApi.new
delivery_note_id = 'delivery_note_id_example' # String | 

begin
  
  result = api_instance.pursue_delivery_note(delivery_note_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->pursue_delivery_note: #{e}"
end
```

#### Using the pursue_delivery_note_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> pursue_delivery_note_with_http_info(delivery_note_id)

```ruby
begin
  
  data, status_code, headers = api_instance.pursue_delivery_note_with_http_info(delivery_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryNoteApi->pursue_delivery_note_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_note_id** | **String** |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

