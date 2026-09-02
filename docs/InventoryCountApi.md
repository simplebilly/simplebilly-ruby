# SimplebillyApi::InventoryCountApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_inventory_count**](InventoryCountApi.md#create_inventory_count) | **POST** /api/v1/inventory-counts |  |
| [**delete_inventory_count**](InventoryCountApi.md#delete_inventory_count) | **DELETE** /api/v1/inventory-counts/{inventory_count_id} |  |
| [**generate_inventory_count**](InventoryCountApi.md#generate_inventory_count) | **POST** /api/v1/inventory-counts/generate |  |
| [**get_inventory_count**](InventoryCountApi.md#get_inventory_count) | **GET** /api/v1/inventory-counts/{inventory_count_id} |  |
| [**list_inventory_counts**](InventoryCountApi.md#list_inventory_counts) | **GET** /api/v1/inventory-counts/ |  |
| [**update_inventory_count**](InventoryCountApi.md#update_inventory_count) | **PUT** /api/v1/inventory-counts/{inventory_count_id} |  |
| [**update_inventory_count_status**](InventoryCountApi.md#update_inventory_count_status) | **PUT** /api/v1/inventory-counts/{inventory_count_id}/status |  |


## create_inventory_count

> <InventoryCount> create_inventory_count(inventory_count)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryCountApi.new
inventory_count = SimplebillyApi::InventoryCount.new({count_date: Date.today, count_number: 'count_number_example', line_items: 3.56, status: SimplebillyApi::InventoryCountStatus::DRAFT, warehouse_id: 'warehouse_id_example'}) # InventoryCount | 

begin
  
  result = api_instance.create_inventory_count(inventory_count)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->create_inventory_count: #{e}"
end
```

#### Using the create_inventory_count_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InventoryCount>, Integer, Hash)> create_inventory_count_with_http_info(inventory_count)

```ruby
begin
  
  data, status_code, headers = api_instance.create_inventory_count_with_http_info(inventory_count)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InventoryCount>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->create_inventory_count_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inventory_count** | [**InventoryCount**](InventoryCount.md) |  |  |

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_inventory_count

> delete_inventory_count(inventory_count_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryCountApi.new
inventory_count_id = 'inventory_count_id_example' # String | 

begin
  
  api_instance.delete_inventory_count(inventory_count_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->delete_inventory_count: #{e}"
end
```

#### Using the delete_inventory_count_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_inventory_count_with_http_info(inventory_count_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_inventory_count_with_http_info(inventory_count_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->delete_inventory_count_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inventory_count_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## generate_inventory_count

> <InventoryCount> generate_inventory_count(generate_count_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryCountApi.new
generate_count_request = SimplebillyApi::GenerateCountRequest.new({warehouse_id: 'warehouse_id_example'}) # GenerateCountRequest | 

begin
  
  result = api_instance.generate_inventory_count(generate_count_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->generate_inventory_count: #{e}"
end
```

#### Using the generate_inventory_count_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InventoryCount>, Integer, Hash)> generate_inventory_count_with_http_info(generate_count_request)

```ruby
begin
  
  data, status_code, headers = api_instance.generate_inventory_count_with_http_info(generate_count_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InventoryCount>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->generate_inventory_count_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **generate_count_request** | [**GenerateCountRequest**](GenerateCountRequest.md) |  |  |

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_inventory_count

> <InventoryCount> get_inventory_count(inventory_count_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryCountApi.new
inventory_count_id = 'inventory_count_id_example' # String | 

begin
  
  result = api_instance.get_inventory_count(inventory_count_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->get_inventory_count: #{e}"
end
```

#### Using the get_inventory_count_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InventoryCount>, Integer, Hash)> get_inventory_count_with_http_info(inventory_count_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_inventory_count_with_http_info(inventory_count_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InventoryCount>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->get_inventory_count_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inventory_count_id** | **String** |  |  |

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_inventory_counts

> <Array<InventoryCount>> list_inventory_counts(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryCountApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  warehouse_id: 'warehouse_id_example' # String | 
}

begin
  
  result = api_instance.list_inventory_counts(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->list_inventory_counts: #{e}"
end
```

#### Using the list_inventory_counts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<InventoryCount>>, Integer, Hash)> list_inventory_counts_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_inventory_counts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<InventoryCount>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->list_inventory_counts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **warehouse_id** | **String** |  | [optional] |

### Return type

[**Array&lt;InventoryCount&gt;**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_inventory_count

> <InventoryCount> update_inventory_count(inventory_count_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryCountApi.new
inventory_count_id = 'inventory_count_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_inventory_count(inventory_count_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->update_inventory_count: #{e}"
end
```

#### Using the update_inventory_count_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InventoryCount>, Integer, Hash)> update_inventory_count_with_http_info(inventory_count_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_inventory_count_with_http_info(inventory_count_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InventoryCount>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->update_inventory_count_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inventory_count_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_inventory_count_status

> <InventoryCount> update_inventory_count_status(inventory_count_id, inventory_count_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryCountApi.new
inventory_count_id = 'inventory_count_id_example' # String | 
inventory_count_status_update = SimplebillyApi::InventoryCountStatusUpdate.new({status: 'status_example'}) # InventoryCountStatusUpdate | 

begin
  
  result = api_instance.update_inventory_count_status(inventory_count_id, inventory_count_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->update_inventory_count_status: #{e}"
end
```

#### Using the update_inventory_count_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InventoryCount>, Integer, Hash)> update_inventory_count_status_with_http_info(inventory_count_id, inventory_count_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_inventory_count_status_with_http_info(inventory_count_id, inventory_count_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InventoryCount>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryCountApi->update_inventory_count_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inventory_count_id** | **String** |  |  |
| **inventory_count_status_update** | [**InventoryCountStatusUpdate**](InventoryCountStatusUpdate.md) |  |  |

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

