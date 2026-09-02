# SimplebillyApi::ContactApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_schema**](ContactApi.md#contact_schema) | **GET** /api/v1/contacts/schema | Serve JSON Schema for client-side validation |
| [**contact_timeline**](ContactApi.md#contact_timeline) | **GET** /api/v1/contacts/{contact_id}/timeline | Get the full per-contact timeline (Xentral §4.6/4.7). |
| [**create_contact**](ContactApi.md#create_contact) | **POST** /api/v1/contacts | Create contact |
| [**delete_contact**](ContactApi.md#delete_contact) | **DELETE** /api/v1/contacts/{contact_id} | Soft-delete contact |
| [**get_contact**](ContactApi.md#get_contact) | **GET** /api/v1/contacts/{contact_id} | Get single contact |
| [**list_contacts**](ContactApi.md#list_contacts) | **GET** /api/v1/contacts | List contacts with search, type filter, and pagination |
| [**sales_volume**](ContactApi.md#sales_volume) | **GET** /api/v1/contacts/sales-volume | Sales volume per contact |
| [**update_contact**](ContactApi.md#update_contact) | **PUT** /api/v1/contacts/{contact_id} | Update contact |


## contact_schema

> Object contact_schema

Serve JSON Schema for client-side validation

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new

begin
  # Serve JSON Schema for client-side validation
  result = api_instance.contact_schema
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->contact_schema: #{e}"
end
```

#### Using the contact_schema_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> contact_schema_with_http_info

```ruby
begin
  # Serve JSON Schema for client-side validation
  data, status_code, headers = api_instance.contact_schema_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->contact_schema_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## contact_timeline

> <ContactTimelineResponse> contact_timeline(contact_id)

Get the full per-contact timeline (Xentral §4.6/4.7).

Aggregates communications, quotations, orders, invoices and uploaded documents for a contact, merged into a single reverse-chronological feed.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new
contact_id = 'contact_id_example' # String | 

begin
  # Get the full per-contact timeline (Xentral §4.6/4.7).
  result = api_instance.contact_timeline(contact_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->contact_timeline: #{e}"
end
```

#### Using the contact_timeline_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ContactTimelineResponse>, Integer, Hash)> contact_timeline_with_http_info(contact_id)

```ruby
begin
  # Get the full per-contact timeline (Xentral §4.6/4.7).
  data, status_code, headers = api_instance.contact_timeline_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ContactTimelineResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->contact_timeline_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

[**ContactTimelineResponse**](ContactTimelineResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_contact

> <Contact> create_contact(body)

Create contact

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new
body = 3.56 # Object | 

begin
  # Create contact
  result = api_instance.create_contact(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->create_contact: #{e}"
end
```

#### Using the create_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Contact>, Integer, Hash)> create_contact_with_http_info(body)

```ruby
begin
  # Create contact
  data, status_code, headers = api_instance.create_contact_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Contact>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->create_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_contact

> delete_contact(contact_id)

Soft-delete contact

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new
contact_id = 'contact_id_example' # String | 

begin
  # Soft-delete contact
  api_instance.delete_contact(contact_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->delete_contact: #{e}"
end
```

#### Using the delete_contact_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_contact_with_http_info(contact_id)

```ruby
begin
  # Soft-delete contact
  data, status_code, headers = api_instance.delete_contact_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->delete_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_contact

> <Contact> get_contact(contact_id)

Get single contact

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new
contact_id = 'contact_id_example' # String | 

begin
  # Get single contact
  result = api_instance.get_contact(contact_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->get_contact: #{e}"
end
```

#### Using the get_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Contact>, Integer, Hash)> get_contact_with_http_info(contact_id)

```ruby
begin
  # Get single contact
  data, status_code, headers = api_instance.get_contact_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Contact>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->get_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_contacts

> <Array<Contact>> list_contacts(opts)

List contacts with search, type filter, and pagination

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  contact_type: 'contact_type_example', # String | 
  tag: 'tag_example' # String | 
}

begin
  # List contacts with search, type filter, and pagination
  result = api_instance.list_contacts(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->list_contacts: #{e}"
end
```

#### Using the list_contacts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Contact>>, Integer, Hash)> list_contacts_with_http_info(opts)

```ruby
begin
  # List contacts with search, type filter, and pagination
  data, status_code, headers = api_instance.list_contacts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Contact>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->list_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **contact_type** | **String** |  | [optional] |
| **tag** | **String** |  | [optional] |

### Return type

[**Array&lt;Contact&gt;**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## sales_volume

> <SalesVolumeReport> sales_volume(opts)

Sales volume per contact

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  contact_type: 'contact_type_example', # String | 
  tag: 'tag_example' # String | 
}

begin
  # Sales volume per contact
  result = api_instance.sales_volume(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->sales_volume: #{e}"
end
```

#### Using the sales_volume_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SalesVolumeReport>, Integer, Hash)> sales_volume_with_http_info(opts)

```ruby
begin
  # Sales volume per contact
  data, status_code, headers = api_instance.sales_volume_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SalesVolumeReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->sales_volume_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **contact_type** | **String** |  | [optional] |
| **tag** | **String** |  | [optional] |

### Return type

[**SalesVolumeReport**](SalesVolumeReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_contact

> <Contact> update_contact(contact_id, body)

Update contact

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ContactApi.new
contact_id = 'contact_id_example' # String | 
body = 3.56 # Object | 

begin
  # Update contact
  result = api_instance.update_contact(contact_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->update_contact: #{e}"
end
```

#### Using the update_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Contact>, Integer, Hash)> update_contact_with_http_info(contact_id, body)

```ruby
begin
  # Update contact
  data, status_code, headers = api_instance.update_contact_with_http_info(contact_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Contact>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ContactApi->update_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

