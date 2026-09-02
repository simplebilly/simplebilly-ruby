# SimplebillyApi::LegalDocumentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_legal_documents**](LegalDocumentApi.md#get_legal_documents) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access. |
| [**reset_legal_documents**](LegalDocumentApi.md#reset_legal_documents) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list. |
| [**upsert_legal_documents**](LegalDocumentApi.md#upsert_legal_documents) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list. |


## get_legal_documents

> <Array<LegalDocument>> get_legal_documents

List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::LegalDocumentApi.new

begin
  # List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
  result = api_instance.get_legal_documents
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LegalDocumentApi->get_legal_documents: #{e}"
end
```

#### Using the get_legal_documents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<LegalDocument>>, Integer, Hash)> get_legal_documents_with_http_info

```ruby
begin
  # List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
  data, status_code, headers = api_instance.get_legal_documents_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<LegalDocument>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LegalDocumentApi->get_legal_documents_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reset_legal_documents

> <Array<LegalDocument>> reset_legal_documents(legal_document_reset)

Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::LegalDocumentApi.new
legal_document_reset = SimplebillyApi::LegalDocumentReset.new # LegalDocumentReset | 

begin
  # Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
  result = api_instance.reset_legal_documents(legal_document_reset)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LegalDocumentApi->reset_legal_documents: #{e}"
end
```

#### Using the reset_legal_documents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<LegalDocument>>, Integer, Hash)> reset_legal_documents_with_http_info(legal_document_reset)

```ruby
begin
  # Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
  data, status_code, headers = api_instance.reset_legal_documents_with_http_info(legal_document_reset)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<LegalDocument>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LegalDocumentApi->reset_legal_documents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **legal_document_reset** | [**LegalDocumentReset**](LegalDocumentReset.md) |  |  |

### Return type

[**Array&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## upsert_legal_documents

> <Array<LegalDocument>> upsert_legal_documents(legal_document_upsert)

Upsert legal documents per (doc_type, lang). Returns the full tenant list.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::LegalDocumentApi.new
legal_document_upsert = [SimplebillyApi::LegalDocumentUpsert.new({content: 'content_example', doc_type: 'doc_type_example', lang: 'lang_example', title: 'title_example'})] # Array<LegalDocumentUpsert> | 

begin
  # Upsert legal documents per (doc_type, lang). Returns the full tenant list.
  result = api_instance.upsert_legal_documents(legal_document_upsert)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LegalDocumentApi->upsert_legal_documents: #{e}"
end
```

#### Using the upsert_legal_documents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<LegalDocument>>, Integer, Hash)> upsert_legal_documents_with_http_info(legal_document_upsert)

```ruby
begin
  # Upsert legal documents per (doc_type, lang). Returns the full tenant list.
  data, status_code, headers = api_instance.upsert_legal_documents_with_http_info(legal_document_upsert)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<LegalDocument>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LegalDocumentApi->upsert_legal_documents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **legal_document_upsert** | [**Array&lt;LegalDocumentUpsert&gt;**](LegalDocumentUpsert.md) |  |  |

### Return type

[**Array&lt;LegalDocument&gt;**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

