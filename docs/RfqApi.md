# SimplebillyApi::RfqApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**convert_rfq**](RfqApi.md#convert_rfq) | **POST** /api/v1/rfqs/{rfq_id}/convert | Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as &#x60;converted&#x60;. |
| [**create_rfq**](RfqApi.md#create_rfq) | **POST** /api/v1/rfqs |  |
| [**delete_rfq**](RfqApi.md#delete_rfq) | **DELETE** /api/v1/rfqs/{rfq_id} |  |
| [**get_rfq**](RfqApi.md#get_rfq) | **GET** /api/v1/rfqs/{rfq_id} |  |
| [**list_rfqs**](RfqApi.md#list_rfqs) | **GET** /api/v1/rfqs/ |  |
| [**update_rfq**](RfqApi.md#update_rfq) | **PUT** /api/v1/rfqs/{rfq_id} |  |
| [**update_rfq_status**](RfqApi.md#update_rfq_status) | **PUT** /api/v1/rfqs/{rfq_id}/status |  |


## convert_rfq

> Object convert_rfq(rfq_id)

Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RfqApi.new
rfq_id = 'rfq_id_example' # String | 

begin
  # Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.
  result = api_instance.convert_rfq(rfq_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->convert_rfq: #{e}"
end
```

#### Using the convert_rfq_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> convert_rfq_with_http_info(rfq_id)

```ruby
begin
  # Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.
  data, status_code, headers = api_instance.convert_rfq_with_http_info(rfq_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->convert_rfq_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rfq_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_rfq

> <Rfq> create_rfq(rfq)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RfqApi.new
rfq = SimplebillyApi::Rfq.new({line_items: 3.56, requested_date: Date.today, rfq_number: 'rfq_number_example', status: SimplebillyApi::RfqStatus::DRAFT}) # Rfq | 

begin
  
  result = api_instance.create_rfq(rfq)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->create_rfq: #{e}"
end
```

#### Using the create_rfq_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Rfq>, Integer, Hash)> create_rfq_with_http_info(rfq)

```ruby
begin
  
  data, status_code, headers = api_instance.create_rfq_with_http_info(rfq)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Rfq>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->create_rfq_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rfq** | [**Rfq**](Rfq.md) |  |  |

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_rfq

> delete_rfq(rfq_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RfqApi.new
rfq_id = 'rfq_id_example' # String | 

begin
  
  api_instance.delete_rfq(rfq_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->delete_rfq: #{e}"
end
```

#### Using the delete_rfq_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_rfq_with_http_info(rfq_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_rfq_with_http_info(rfq_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->delete_rfq_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rfq_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_rfq

> <Rfq> get_rfq(rfq_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RfqApi.new
rfq_id = 'rfq_id_example' # String | 

begin
  
  result = api_instance.get_rfq(rfq_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->get_rfq: #{e}"
end
```

#### Using the get_rfq_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Rfq>, Integer, Hash)> get_rfq_with_http_info(rfq_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_rfq_with_http_info(rfq_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Rfq>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->get_rfq_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rfq_id** | **String** |  |  |

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_rfqs

> <Array<Rfq>> list_rfqs(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RfqApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  supplier_name: 'supplier_name_example' # String | 
}

begin
  
  result = api_instance.list_rfqs(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->list_rfqs: #{e}"
end
```

#### Using the list_rfqs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Rfq>>, Integer, Hash)> list_rfqs_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_rfqs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Rfq>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->list_rfqs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **supplier_name** | **String** |  | [optional] |

### Return type

[**Array&lt;Rfq&gt;**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_rfq

> <Rfq> update_rfq(rfq_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RfqApi.new
rfq_id = 'rfq_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_rfq(rfq_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->update_rfq: #{e}"
end
```

#### Using the update_rfq_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Rfq>, Integer, Hash)> update_rfq_with_http_info(rfq_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_rfq_with_http_info(rfq_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Rfq>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->update_rfq_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rfq_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_rfq_status

> <Rfq> update_rfq_status(rfq_id, rfq_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RfqApi.new
rfq_id = 'rfq_id_example' # String | 
rfq_status_update = SimplebillyApi::RfqStatusUpdate.new({status: 'status_example'}) # RfqStatusUpdate | 

begin
  
  result = api_instance.update_rfq_status(rfq_id, rfq_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->update_rfq_status: #{e}"
end
```

#### Using the update_rfq_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Rfq>, Integer, Hash)> update_rfq_status_with_http_info(rfq_id, rfq_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_rfq_status_with_http_info(rfq_id, rfq_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Rfq>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RfqApi->update_rfq_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rfq_id** | **String** |  |  |
| **rfq_status_update** | [**RfqStatusUpdate**](RfqStatusUpdate.md) |  |  |

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

