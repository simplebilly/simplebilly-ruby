# SimplebillyApi::SupplierConditionApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_supplier_condition**](SupplierConditionApi.md#create_supplier_condition) | **POST** /api/v1/supplier-conditions |  |
| [**delete_supplier_condition**](SupplierConditionApi.md#delete_supplier_condition) | **DELETE** /api/v1/supplier-conditions/{supplier_condition_id} |  |
| [**get_supplier_condition**](SupplierConditionApi.md#get_supplier_condition) | **GET** /api/v1/supplier-conditions/{supplier_condition_id} |  |
| [**list_supplier_conditions**](SupplierConditionApi.md#list_supplier_conditions) | **GET** /api/v1/supplier-conditions/ |  |
| [**update_supplier_condition**](SupplierConditionApi.md#update_supplier_condition) | **PUT** /api/v1/supplier-conditions/{supplier_condition_id} |  |


## create_supplier_condition

> <SupplierCondition> create_supplier_condition(supplier_condition_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierConditionApi.new
supplier_condition_create = SimplebillyApi::SupplierConditionCreate.new({currency: 'currency_example', supplier_contact_id: 'supplier_contact_id_example'}) # SupplierConditionCreate | 

begin
  
  result = api_instance.create_supplier_condition(supplier_condition_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->create_supplier_condition: #{e}"
end
```

#### Using the create_supplier_condition_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupplierCondition>, Integer, Hash)> create_supplier_condition_with_http_info(supplier_condition_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_supplier_condition_with_http_info(supplier_condition_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupplierCondition>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->create_supplier_condition_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_condition_create** | [**SupplierConditionCreate**](SupplierConditionCreate.md) |  |  |

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_supplier_condition

> delete_supplier_condition(supplier_condition_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierConditionApi.new
supplier_condition_id = 'supplier_condition_id_example' # String | 

begin
  
  api_instance.delete_supplier_condition(supplier_condition_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->delete_supplier_condition: #{e}"
end
```

#### Using the delete_supplier_condition_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_supplier_condition_with_http_info(supplier_condition_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_supplier_condition_with_http_info(supplier_condition_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->delete_supplier_condition_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_condition_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_supplier_condition

> <SupplierCondition> get_supplier_condition(supplier_condition_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierConditionApi.new
supplier_condition_id = 'supplier_condition_id_example' # String | 

begin
  
  result = api_instance.get_supplier_condition(supplier_condition_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->get_supplier_condition: #{e}"
end
```

#### Using the get_supplier_condition_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupplierCondition>, Integer, Hash)> get_supplier_condition_with_http_info(supplier_condition_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_supplier_condition_with_http_info(supplier_condition_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupplierCondition>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->get_supplier_condition_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_condition_id** | **String** |  |  |

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_supplier_conditions

> <Array<SupplierCondition>> list_supplier_conditions(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierConditionApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  supplier_contact_id: 'supplier_contact_id_example', # String | 
  search: 'search_example' # String | 
}

begin
  
  result = api_instance.list_supplier_conditions(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->list_supplier_conditions: #{e}"
end
```

#### Using the list_supplier_conditions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<SupplierCondition>>, Integer, Hash)> list_supplier_conditions_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_supplier_conditions_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<SupplierCondition>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->list_supplier_conditions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **supplier_contact_id** | **String** |  | [optional] |
| **search** | **String** |  | [optional] |

### Return type

[**Array&lt;SupplierCondition&gt;**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_supplier_condition

> <SupplierCondition> update_supplier_condition(supplier_condition_id, supplier_condition_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupplierConditionApi.new
supplier_condition_id = 'supplier_condition_id_example' # String | 
supplier_condition_update = SimplebillyApi::SupplierConditionUpdate.new # SupplierConditionUpdate | 

begin
  
  result = api_instance.update_supplier_condition(supplier_condition_id, supplier_condition_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->update_supplier_condition: #{e}"
end
```

#### Using the update_supplier_condition_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupplierCondition>, Integer, Hash)> update_supplier_condition_with_http_info(supplier_condition_id, supplier_condition_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_supplier_condition_with_http_info(supplier_condition_id, supplier_condition_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupplierCondition>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupplierConditionApi->update_supplier_condition_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supplier_condition_id** | **String** |  |  |
| **supplier_condition_update** | [**SupplierConditionUpdate**](SupplierConditionUpdate.md) |  |  |

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

