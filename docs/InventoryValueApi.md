# SimplebillyApi::InventoryValueApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_inventory_value_api**](InventoryValueApi.md#get_inventory_value_api) | **GET** /api/v1/bookkeeping/inventory-value |  |
| [**record_inventory_value_api**](InventoryValueApi.md#record_inventory_value_api) | **POST** /api/v1/bookkeeping/inventory-value/record |  |


## get_inventory_value_api

> <CurrentInventoryValue> get_inventory_value_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryValueApi.new

begin
  
  result = api_instance.get_inventory_value_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryValueApi->get_inventory_value_api: #{e}"
end
```

#### Using the get_inventory_value_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CurrentInventoryValue>, Integer, Hash)> get_inventory_value_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.get_inventory_value_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CurrentInventoryValue>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryValueApi->get_inventory_value_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CurrentInventoryValue**](CurrentInventoryValue.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## record_inventory_value_api

> <InventoryValuePoint> record_inventory_value_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InventoryValueApi.new

begin
  
  result = api_instance.record_inventory_value_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryValueApi->record_inventory_value_api: #{e}"
end
```

#### Using the record_inventory_value_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InventoryValuePoint>, Integer, Hash)> record_inventory_value_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.record_inventory_value_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InventoryValuePoint>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InventoryValueApi->record_inventory_value_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**InventoryValuePoint**](InventoryValuePoint.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

