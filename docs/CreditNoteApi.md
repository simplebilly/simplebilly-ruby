# SimplebillyApi::CreditNoteApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_credit_note**](CreditNoteApi.md#create_credit_note) | **POST** /api/v1/credit-notes |  |
| [**download_credit_note_pdf**](CreditNoteApi.md#download_credit_note_pdf) | **GET** /api/v1/credit-notes/{credit_note_id}/pdf |  |
| [**get_credit_note**](CreditNoteApi.md#get_credit_note) | **GET** /api/v1/credit-notes/{credit_note_id} |  |
| [**list_credit_notes**](CreditNoteApi.md#list_credit_notes) | **GET** /api/v1/credit-notes/ |  |


## create_credit_note

> <Invoice> create_credit_note(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CreditNoteApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.create_credit_note(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->create_credit_note: #{e}"
end
```

#### Using the create_credit_note_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> create_credit_note_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.create_credit_note_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->create_credit_note_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## download_credit_note_pdf

> download_credit_note_pdf(credit_note_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CreditNoteApi.new
credit_note_id = 'credit_note_id_example' # String | 

begin
  
  api_instance.download_credit_note_pdf(credit_note_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->download_credit_note_pdf: #{e}"
end
```

#### Using the download_credit_note_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> download_credit_note_pdf_with_http_info(credit_note_id)

```ruby
begin
  
  data, status_code, headers = api_instance.download_credit_note_pdf_with_http_info(credit_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->download_credit_note_pdf_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credit_note_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json


## get_credit_note

> <Invoice> get_credit_note(credit_note_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CreditNoteApi.new
credit_note_id = 'credit_note_id_example' # String | 

begin
  
  result = api_instance.get_credit_note(credit_note_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->get_credit_note: #{e}"
end
```

#### Using the get_credit_note_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Invoice>, Integer, Hash)> get_credit_note_with_http_info(credit_note_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_credit_note_with_http_info(credit_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Invoice>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->get_credit_note_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credit_note_id** | **String** |  |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_credit_notes

> <Array<Invoice>> list_credit_notes(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CreditNoteApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.list_credit_notes(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->list_credit_notes: #{e}"
end
```

#### Using the list_credit_notes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Invoice>>, Integer, Hash)> list_credit_notes_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_credit_notes_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Invoice>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreditNoteApi->list_credit_notes_with_http_info: #{e}"
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

