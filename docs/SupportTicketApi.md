# SimplebillyApi::SupportTicketApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_ticket_api**](SupportTicketApi.md#create_ticket_api) | **POST** /api/v1/support/tickets |  |
| [**delete_ticket_api**](SupportTicketApi.md#delete_ticket_api) | **DELETE** /api/v1/support/tickets/{ticket_id} |  |
| [**get_ticket_api**](SupportTicketApi.md#get_ticket_api) | **GET** /api/v1/support/tickets/{ticket_id} |  |
| [**list_tickets_api**](SupportTicketApi.md#list_tickets_api) | **GET** /api/v1/support/tickets |  |
| [**update_ticket_api**](SupportTicketApi.md#update_ticket_api) | **PUT** /api/v1/support/tickets/{ticket_id} |  |


## create_ticket_api

> <SupportTicket> create_ticket_api(create_ticket_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportTicketApi.new
create_ticket_request = SimplebillyApi::CreateTicketRequest.new({message_body: 'message_body_example', subject: 'subject_example'}) # CreateTicketRequest | 

begin
  
  result = api_instance.create_ticket_api(create_ticket_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->create_ticket_api: #{e}"
end
```

#### Using the create_ticket_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupportTicket>, Integer, Hash)> create_ticket_api_with_http_info(create_ticket_request)

```ruby
begin
  
  data, status_code, headers = api_instance.create_ticket_api_with_http_info(create_ticket_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupportTicket>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->create_ticket_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_ticket_request** | [**CreateTicketRequest**](CreateTicketRequest.md) |  |  |

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_ticket_api

> delete_ticket_api(ticket_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportTicketApi.new
ticket_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_ticket_api(ticket_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->delete_ticket_api: #{e}"
end
```

#### Using the delete_ticket_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_ticket_api_with_http_info(ticket_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_ticket_api_with_http_info(ticket_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->delete_ticket_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ticket_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_ticket_api

> <SupportTicket> get_ticket_api(ticket_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportTicketApi.new
ticket_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_ticket_api(ticket_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->get_ticket_api: #{e}"
end
```

#### Using the get_ticket_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupportTicket>, Integer, Hash)> get_ticket_api_with_http_info(ticket_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_ticket_api_with_http_info(ticket_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupportTicket>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->get_ticket_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ticket_id** | **String** |  |  |

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_tickets_api

> <Array<SupportTicket>> list_tickets_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportTicketApi.new
opts = {
  status: 'status_example', # String | 
  priority: 'priority_example', # String | 
  assigned_to: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  channel_type: 'channel_type_example', # String | 
  customer_id: 'customer_id_example', # String | 
  search: 'search_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  
  result = api_instance.list_tickets_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->list_tickets_api: #{e}"
end
```

#### Using the list_tickets_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<SupportTicket>>, Integer, Hash)> list_tickets_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_tickets_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<SupportTicket>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->list_tickets_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **priority** | **String** |  | [optional] |
| **assigned_to** | **String** |  | [optional] |
| **channel_type** | **String** |  | [optional] |
| **customer_id** | **String** |  | [optional] |
| **search** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**Array&lt;SupportTicket&gt;**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_ticket_api

> <SupportTicket> update_ticket_api(ticket_id, support_ticket_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportTicketApi.new
ticket_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
support_ticket_update = SimplebillyApi::SupportTicketUpdate.new # SupportTicketUpdate | 

begin
  
  result = api_instance.update_ticket_api(ticket_id, support_ticket_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->update_ticket_api: #{e}"
end
```

#### Using the update_ticket_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupportTicket>, Integer, Hash)> update_ticket_api_with_http_info(ticket_id, support_ticket_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_ticket_api_with_http_info(ticket_id, support_ticket_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupportTicket>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportTicketApi->update_ticket_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ticket_id** | **String** |  |  |
| **support_ticket_update** | [**SupportTicketUpdate**](SupportTicketUpdate.md) |  |  |

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

