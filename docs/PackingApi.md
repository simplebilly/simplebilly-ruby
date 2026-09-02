# SimplebillyApi::PackingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**complete_packing**](PackingApi.md#complete_packing) | **POST** /api/v1/packing/{order_number}/complete | Mark packing as complete and transition order to shipped |
| [**get_packing_queue**](PackingApi.md#get_packing_queue) | **GET** /api/v1/packing/queue | Get the packing queue - orders ready for packing |
| [**print_delivery_note**](PackingApi.md#print_delivery_note) | **POST** /api/v1/packing/{order_number}/print-delivery-note | Print delivery note (Lieferschein) for an order |
| [**print_label**](PackingApi.md#print_label) | **POST** /api/v1/packing/{order_number}/print-label | Print shipping label for an order |
| [**record_packing_video**](PackingApi.md#record_packing_video) | **POST** /api/v1/packing/{order_number}/record-video | Record video of packing process |


## complete_packing

> <PackingCompleteResponse> complete_packing(order_number, packing_complete_request)

Mark packing as complete and transition order to shipped

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PackingApi.new
order_number = 'order_number_example' # String | 
packing_complete_request = SimplebillyApi::PackingCompleteRequest.new({order_number: 'order_number_example'}) # PackingCompleteRequest | 

begin
  # Mark packing as complete and transition order to shipped
  result = api_instance.complete_packing(order_number, packing_complete_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->complete_packing: #{e}"
end
```

#### Using the complete_packing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PackingCompleteResponse>, Integer, Hash)> complete_packing_with_http_info(order_number, packing_complete_request)

```ruby
begin
  # Mark packing as complete and transition order to shipped
  data, status_code, headers = api_instance.complete_packing_with_http_info(order_number, packing_complete_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PackingCompleteResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->complete_packing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |
| **packing_complete_request** | [**PackingCompleteRequest**](PackingCompleteRequest.md) |  |  |

### Return type

[**PackingCompleteResponse**](PackingCompleteResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_packing_queue

> <PackingQueue> get_packing_queue(opts)

Get the packing queue - orders ready for packing

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PackingApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example' # String | 
}

begin
  # Get the packing queue - orders ready for packing
  result = api_instance.get_packing_queue(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->get_packing_queue: #{e}"
end
```

#### Using the get_packing_queue_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PackingQueue>, Integer, Hash)> get_packing_queue_with_http_info(opts)

```ruby
begin
  # Get the packing queue - orders ready for packing
  data, status_code, headers = api_instance.get_packing_queue_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PackingQueue>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->get_packing_queue_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |

### Return type

[**PackingQueue**](PackingQueue.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## print_delivery_note

> <PrintDeliveryNoteResponse> print_delivery_note(order_number)

Print delivery note (Lieferschein) for an order

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PackingApi.new
order_number = 'order_number_example' # String | 

begin
  # Print delivery note (Lieferschein) for an order
  result = api_instance.print_delivery_note(order_number)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->print_delivery_note: #{e}"
end
```

#### Using the print_delivery_note_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PrintDeliveryNoteResponse>, Integer, Hash)> print_delivery_note_with_http_info(order_number)

```ruby
begin
  # Print delivery note (Lieferschein) for an order
  data, status_code, headers = api_instance.print_delivery_note_with_http_info(order_number)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PrintDeliveryNoteResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->print_delivery_note_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |

### Return type

[**PrintDeliveryNoteResponse**](PrintDeliveryNoteResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## print_label

> <PrintLabelResponse> print_label(order_number)

Print shipping label for an order

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PackingApi.new
order_number = 'order_number_example' # String | 

begin
  # Print shipping label for an order
  result = api_instance.print_label(order_number)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->print_label: #{e}"
end
```

#### Using the print_label_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PrintLabelResponse>, Integer, Hash)> print_label_with_http_info(order_number)

```ruby
begin
  # Print shipping label for an order
  data, status_code, headers = api_instance.print_label_with_http_info(order_number)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PrintLabelResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->print_label_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |

### Return type

[**PrintLabelResponse**](PrintLabelResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## record_packing_video

> <PackingVideoResponse> record_packing_video(order_number, body)

Record video of packing process

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PackingApi.new
order_number = 'order_number_example' # String | 
body = 3.56 # Object | 

begin
  # Record video of packing process
  result = api_instance.record_packing_video(order_number, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->record_packing_video: #{e}"
end
```

#### Using the record_packing_video_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PackingVideoResponse>, Integer, Hash)> record_packing_video_with_http_info(order_number, body)

```ruby
begin
  # Record video of packing process
  data, status_code, headers = api_instance.record_packing_video_with_http_info(order_number, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PackingVideoResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PackingApi->record_packing_video_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**PackingVideoResponse**](PackingVideoResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

