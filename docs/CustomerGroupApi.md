# SimplebillyApi::CustomerGroupApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_group_members**](CustomerGroupApi.md#add_group_members) | **POST** /api/v1/customer-groups/{customer_group_id}/members |  |
| [**create_customer_group**](CustomerGroupApi.md#create_customer_group) | **POST** /api/v1/customer-groups |  |
| [**delete_customer_group**](CustomerGroupApi.md#delete_customer_group) | **DELETE** /api/v1/customer-groups/{customer_group_id} |  |
| [**get_customer_group**](CustomerGroupApi.md#get_customer_group) | **GET** /api/v1/customer-groups/{customer_group_id} |  |
| [**list_customer_groups**](CustomerGroupApi.md#list_customer_groups) | **GET** /api/v1/customer-groups/ |  |
| [**update_customer_group**](CustomerGroupApi.md#update_customer_group) | **PUT** /api/v1/customer-groups/{customer_group_id} |  |


## add_group_members

> <CustomerGroup> add_group_members(customer_group_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerGroupApi.new
customer_group_id = 'customer_group_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.add_group_members(customer_group_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->add_group_members: #{e}"
end
```

#### Using the add_group_members_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerGroup>, Integer, Hash)> add_group_members_with_http_info(customer_group_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.add_group_members_with_http_info(customer_group_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerGroup>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->add_group_members_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_group_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_customer_group

> <CustomerGroup> create_customer_group(customer_group_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerGroupApi.new
customer_group_create = SimplebillyApi::CustomerGroupCreate.new({name: 'name_example'}) # CustomerGroupCreate | 

begin
  
  result = api_instance.create_customer_group(customer_group_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->create_customer_group: #{e}"
end
```

#### Using the create_customer_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerGroup>, Integer, Hash)> create_customer_group_with_http_info(customer_group_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_customer_group_with_http_info(customer_group_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerGroup>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->create_customer_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_group_create** | [**CustomerGroupCreate**](CustomerGroupCreate.md) |  |  |

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_customer_group

> delete_customer_group(customer_group_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerGroupApi.new
customer_group_id = 'customer_group_id_example' # String | 

begin
  
  api_instance.delete_customer_group(customer_group_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->delete_customer_group: #{e}"
end
```

#### Using the delete_customer_group_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_customer_group_with_http_info(customer_group_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_customer_group_with_http_info(customer_group_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->delete_customer_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_group_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_customer_group

> <CustomerGroup> get_customer_group(customer_group_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerGroupApi.new
customer_group_id = 'customer_group_id_example' # String | 

begin
  
  result = api_instance.get_customer_group(customer_group_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->get_customer_group: #{e}"
end
```

#### Using the get_customer_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerGroup>, Integer, Hash)> get_customer_group_with_http_info(customer_group_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_customer_group_with_http_info(customer_group_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerGroup>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->get_customer_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_group_id** | **String** |  |  |

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_customer_groups

> <Array<CustomerGroup>> list_customer_groups(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerGroupApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.list_customer_groups(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->list_customer_groups: #{e}"
end
```

#### Using the list_customer_groups_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CustomerGroup>>, Integer, Hash)> list_customer_groups_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_customer_groups_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CustomerGroup>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->list_customer_groups_with_http_info: #{e}"
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

[**Array&lt;CustomerGroup&gt;**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_customer_group

> <CustomerGroup> update_customer_group(customer_group_id, customer_group_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CustomerGroupApi.new
customer_group_id = 'customer_group_id_example' # String | 
customer_group_update = SimplebillyApi::CustomerGroupUpdate.new # CustomerGroupUpdate | 

begin
  
  result = api_instance.update_customer_group(customer_group_id, customer_group_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->update_customer_group: #{e}"
end
```

#### Using the update_customer_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerGroup>, Integer, Hash)> update_customer_group_with_http_info(customer_group_id, customer_group_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_customer_group_with_http_info(customer_group_id, customer_group_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerGroup>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CustomerGroupApi->update_customer_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_group_id** | **String** |  |  |
| **customer_group_update** | [**CustomerGroupUpdate**](CustomerGroupUpdate.md) |  |  |

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

