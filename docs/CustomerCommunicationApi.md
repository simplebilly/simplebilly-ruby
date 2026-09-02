# SimplebillyApi::CustomerCommunicationApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_communication**](CustomerCommunicationApi.md#create_communication) | **POST** /api/v1/communications |  |
| [**customercommunication_restore**](CustomerCommunicationApi.md#customercommunication_restore) | **POST** /api/v1/communications/{communication_id}/restore |  |
| [**delete_communication**](CustomerCommunicationApi.md#delete_communication) | **DELETE** /api/v1/communications/{communication_id} |  |
| [**get_communication**](CustomerCommunicationApi.md#get_communication) | **GET** /api/v1/communications/{communication_id} |  |
| [**get_contact_history**](CustomerCommunicationApi.md#get_contact_history) | **GET** /api/v1/contacts/{contact_id}/communications |  |
| [**list_communications**](CustomerCommunicationApi.md#list_communications) | **GET** /api/v1/communications/ |  |
| [**update_communication**](CustomerCommunicationApi.md#update_communication) | **PUT** /api/v1/communications/{communication_id} |  |


## create_communication

> <CustomerCommunication> create_communication(customer_communication_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerCommunicationApi.new
customer_communication_create = SimplebillyApi::CustomerCommunicationCreate.new({channel: SimplebillyApi::CommunicationChannel::EMAIL, contact_id: 'contact_id_example', direction: SimplebillyApi::CommunicationDirection::INBOUND}) # CustomerCommunicationCreate | 

begin
  
  result = api_instance.create_communication(customer_communication_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->create_communication: #{e}"
end
```

#### Using the create_communication_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerCommunication>, Integer, Hash)> create_communication_with_http_info(customer_communication_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_communication_with_http_info(customer_communication_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerCommunication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->create_communication_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_communication_create** | [**CustomerCommunicationCreate**](CustomerCommunicationCreate.md) |  |  |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## customercommunication_restore

> <CustomerCommunication> customercommunication_restore(communication_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerCommunicationApi.new
communication_id = 'communication_id_example' # String | 

begin
  
  result = api_instance.customercommunication_restore(communication_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->customercommunication_restore: #{e}"
end
```

#### Using the customercommunication_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerCommunication>, Integer, Hash)> customercommunication_restore_with_http_info(communication_id)

```ruby
begin
  
  data, status_code, headers = api_instance.customercommunication_restore_with_http_info(communication_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerCommunication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->customercommunication_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **communication_id** | **String** |  |  |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_communication

> delete_communication(communication_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerCommunicationApi.new
communication_id = 'communication_id_example' # String | 

begin
  
  api_instance.delete_communication(communication_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->delete_communication: #{e}"
end
```

#### Using the delete_communication_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_communication_with_http_info(communication_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_communication_with_http_info(communication_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->delete_communication_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **communication_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_communication

> <CustomerCommunication> get_communication(communication_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerCommunicationApi.new
communication_id = 'communication_id_example' # String | 

begin
  
  result = api_instance.get_communication(communication_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->get_communication: #{e}"
end
```

#### Using the get_communication_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerCommunication>, Integer, Hash)> get_communication_with_http_info(communication_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_communication_with_http_info(communication_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerCommunication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->get_communication_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **communication_id** | **String** |  |  |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_contact_history

> <ContactHistoryResponse> get_contact_history(contact_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerCommunicationApi.new
contact_id = 'contact_id_example' # String | 

begin
  
  result = api_instance.get_contact_history(contact_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->get_contact_history: #{e}"
end
```

#### Using the get_contact_history_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ContactHistoryResponse>, Integer, Hash)> get_contact_history_with_http_info(contact_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_contact_history_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ContactHistoryResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->get_contact_history_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

[**ContactHistoryResponse**](ContactHistoryResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_communications

> <Array<CustomerCommunication>> list_communications(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerCommunicationApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  contact_id: 'contact_id_example', # String | Filter history to a single contact.
  channel: SimplebillyApi::CommunicationChannel::EMAIL, # CommunicationChannel | 
  direction: SimplebillyApi::CommunicationDirection::INBOUND, # CommunicationDirection | 
  from: Date.parse('2013-10-20'), # Date | Only include communications after this ISO date (inclusive).
  to: Date.parse('2013-10-20') # Date | Only include communications before this ISO date (inclusive).
}

begin
  
  result = api_instance.list_communications(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->list_communications: #{e}"
end
```

#### Using the list_communications_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CustomerCommunication>>, Integer, Hash)> list_communications_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_communications_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CustomerCommunication>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->list_communications_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **contact_id** | **String** | Filter history to a single contact. | [optional] |
| **channel** | [**CommunicationChannel**](.md) |  | [optional] |
| **direction** | [**CommunicationDirection**](.md) |  | [optional] |
| **from** | **Date** | Only include communications after this ISO date (inclusive). | [optional] |
| **to** | **Date** | Only include communications before this ISO date (inclusive). | [optional] |

### Return type

[**Array&lt;CustomerCommunication&gt;**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_communication

> <CustomerCommunication> update_communication(communication_id, customer_communication_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerCommunicationApi.new
communication_id = 'communication_id_example' # String | 
customer_communication_update = SimplebillyApi::CustomerCommunicationUpdate.new # CustomerCommunicationUpdate | 

begin
  
  result = api_instance.update_communication(communication_id, customer_communication_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->update_communication: #{e}"
end
```

#### Using the update_communication_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerCommunication>, Integer, Hash)> update_communication_with_http_info(communication_id, customer_communication_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_communication_with_http_info(communication_id, customer_communication_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerCommunication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerCommunicationApi->update_communication_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **communication_id** | **String** |  |  |
| **customer_communication_update** | [**CustomerCommunicationUpdate**](CustomerCommunicationUpdate.md) |  |  |

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

