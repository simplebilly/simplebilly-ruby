# SimplebillyApi::TicketMessageApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_messages_api**](TicketMessageApi.md#list_messages_api) | **GET** /api/v1/support/tickets/{ticket_id}/messages |  |
| [**send_message_api**](TicketMessageApi.md#send_message_api) | **POST** /api/v1/support/tickets/{ticket_id}/messages |  |


## list_messages_api

> <Array<TicketMessage>> list_messages_api(ticket_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TicketMessageApi.new
ticket_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.list_messages_api(ticket_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TicketMessageApi->list_messages_api: #{e}"
end
```

#### Using the list_messages_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<TicketMessage>>, Integer, Hash)> list_messages_api_with_http_info(ticket_id)

```ruby
begin
  
  data, status_code, headers = api_instance.list_messages_api_with_http_info(ticket_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<TicketMessage>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TicketMessageApi->list_messages_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ticket_id** | **String** |  |  |

### Return type

[**Array&lt;TicketMessage&gt;**](TicketMessage.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_message_api

> <TicketMessage> send_message_api(ticket_id, send_message_dto)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TicketMessageApi.new
ticket_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
send_message_dto = SimplebillyApi::SendMessageDto.new({body: 'body_example'}) # SendMessageDto | 

begin
  
  result = api_instance.send_message_api(ticket_id, send_message_dto)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TicketMessageApi->send_message_api: #{e}"
end
```

#### Using the send_message_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TicketMessage>, Integer, Hash)> send_message_api_with_http_info(ticket_id, send_message_dto)

```ruby
begin
  
  data, status_code, headers = api_instance.send_message_api_with_http_info(ticket_id, send_message_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TicketMessage>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TicketMessageApi->send_message_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ticket_id** | **String** |  |  |
| **send_message_dto** | [**SendMessageDto**](SendMessageDto.md) |  |  |

### Return type

[**TicketMessage**](TicketMessage.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

