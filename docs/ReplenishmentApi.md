# SimplebillyApi::ReplenishmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**apply_replenishments**](ReplenishmentApi.md#apply_replenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair. |
| [**get_replenishments**](ReplenishmentApi.md#get_replenishments) | **GET** /api/v1/replenishments |  |


## apply_replenishments

> Object apply_replenishments(opts)

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReplenishmentApi.new
opts = {
  target_warehouse_id: 'target_warehouse_id_example', # String | Warehouse to be replenished. Defaults to the tenant's default warehouse.
  source_warehouse_id: 'source_warehouse_id_example' # String | Restrict source warehouses to this id.
}

begin
  # Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
  result = api_instance.apply_replenishments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReplenishmentApi->apply_replenishments: #{e}"
end
```

#### Using the apply_replenishments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> apply_replenishments_with_http_info(opts)

```ruby
begin
  # Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
  data, status_code, headers = api_instance.apply_replenishments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReplenishmentApi->apply_replenishments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **target_warehouse_id** | **String** | Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] |
| **source_warehouse_id** | **String** | Restrict source warehouses to this id. | [optional] |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_replenishments

> <ReplenishmentResponse> get_replenishments(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReplenishmentApi.new
opts = {
  target_warehouse_id: 'target_warehouse_id_example', # String | Warehouse to be replenished. Defaults to the tenant's default warehouse.
  source_warehouse_id: 'source_warehouse_id_example' # String | Restrict source warehouses to this id.
}

begin
  
  result = api_instance.get_replenishments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReplenishmentApi->get_replenishments: #{e}"
end
```

#### Using the get_replenishments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReplenishmentResponse>, Integer, Hash)> get_replenishments_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_replenishments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReplenishmentResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReplenishmentApi->get_replenishments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **target_warehouse_id** | **String** | Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] |
| **source_warehouse_id** | **String** | Restrict source warehouses to this id. | [optional] |

### Return type

[**ReplenishmentResponse**](ReplenishmentResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

