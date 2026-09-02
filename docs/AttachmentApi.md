# SimplebillyApi::AttachmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**attachment_restore**](AttachmentApi.md#attachment_restore) | **POST** /api/v1/attachments/{id}/restore |  |
| [**create_attachment**](AttachmentApi.md#create_attachment) | **POST** /api/v1/attachments |  |
| [**delete_attachment**](AttachmentApi.md#delete_attachment) | **DELETE** /api/v1/attachments/{id} |  |
| [**get_attachment**](AttachmentApi.md#get_attachment) | **GET** /api/v1/attachments/{id} |  |
| [**list_attachments**](AttachmentApi.md#list_attachments) | **GET** /api/v1/attachments/ |  |
| [**save_attachment_ocr_text**](AttachmentApi.md#save_attachment_ocr_text) | **PUT** /api/v1/attachments/{attachment_id}/ocr-text | Persist client-side OCR output for an attachment. |


## attachment_restore

> <Attachment> attachment_restore(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.attachment_restore(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->attachment_restore: #{e}"
end
```

#### Using the attachment_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Attachment>, Integer, Hash)> attachment_restore_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.attachment_restore_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Attachment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->attachment_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_attachment

> <Attachment> create_attachment(attachment_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentApi.new
attachment_create = SimplebillyApi::AttachmentCreate.new({file_name: 'file_name_example', original_name: 'original_name_example'}) # AttachmentCreate | 

begin
  
  result = api_instance.create_attachment(attachment_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->create_attachment: #{e}"
end
```

#### Using the create_attachment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Attachment>, Integer, Hash)> create_attachment_with_http_info(attachment_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_attachment_with_http_info(attachment_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Attachment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->create_attachment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attachment_create** | [**AttachmentCreate**](AttachmentCreate.md) |  |  |

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_attachment

> delete_attachment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_attachment(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->delete_attachment: #{e}"
end
```

#### Using the delete_attachment_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_attachment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_attachment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->delete_attachment_with_http_info: #{e}"
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


## get_attachment

> <Attachment> get_attachment(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_attachment(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->get_attachment: #{e}"
end
```

#### Using the get_attachment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Attachment>, Integer, Hash)> get_attachment_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_attachment_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Attachment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->get_attachment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_attachments

> <Array<Attachment>> list_attachments(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  contact_id: 'contact_id_example' # String | 
}

begin
  
  result = api_instance.list_attachments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->list_attachments: #{e}"
end
```

#### Using the list_attachments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Attachment>>, Integer, Hash)> list_attachments_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_attachments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Attachment>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->list_attachments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **contact_id** | **String** |  | [optional] |

### Return type

[**Array&lt;Attachment&gt;**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## save_attachment_ocr_text

> <Attachment> save_attachment_ocr_text(attachment_id, ocr_text_request)

Persist client-side OCR output for an attachment.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentApi.new
attachment_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
ocr_text_request = SimplebillyApi::OcrTextRequest.new # OcrTextRequest | 

begin
  # Persist client-side OCR output for an attachment.
  result = api_instance.save_attachment_ocr_text(attachment_id, ocr_text_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->save_attachment_ocr_text: #{e}"
end
```

#### Using the save_attachment_ocr_text_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Attachment>, Integer, Hash)> save_attachment_ocr_text_with_http_info(attachment_id, ocr_text_request)

```ruby
begin
  # Persist client-side OCR output for an attachment.
  data, status_code, headers = api_instance.save_attachment_ocr_text_with_http_info(attachment_id, ocr_text_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Attachment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentApi->save_attachment_ocr_text_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attachment_id** | **String** |  |  |
| **ocr_text_request** | [**OcrTextRequest**](OcrTextRequest.md) |  |  |

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

