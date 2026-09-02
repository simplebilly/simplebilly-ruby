# SimplebillyApi::ShippingThresholdApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_shipping_threshold**](ShippingThresholdApi.md#create_shipping_threshold) | **POST** /api/v1/shipping-thresholds |  |
| [**delete_shipping_threshold**](ShippingThresholdApi.md#delete_shipping_threshold) | **DELETE** /api/v1/shipping-thresholds/{threshold_id} |  |
| [**get_deliverable**](ShippingThresholdApi.md#get_deliverable) | **GET** /api/v1/shipping-thresholds/deliverable |  |
| [**get_shipping_threshold**](ShippingThresholdApi.md#get_shipping_threshold) | **GET** /api/v1/shipping-thresholds/{threshold_id} |  |
| [**list_shipping_thresholds**](ShippingThresholdApi.md#list_shipping_thresholds) | **GET** /api/v1/shipping-thresholds/ |  |
| [**update_shipping_threshold**](ShippingThresholdApi.md#update_shipping_threshold) | **PUT** /api/v1/shipping-thresholds/{threshold_id} |  |


## create_shipping_threshold

> <ShippingThreshold> create_shipping_threshold(shipping_threshold_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingThresholdApi.new
shipping_threshold_create = SimplebillyApi::ShippingThresholdCreate.new({name: 'name_example'}) # ShippingThresholdCreate | 

begin
  
  result = api_instance.create_shipping_threshold(shipping_threshold_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->create_shipping_threshold: #{e}"
end
```

#### Using the create_shipping_threshold_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingThreshold>, Integer, Hash)> create_shipping_threshold_with_http_info(shipping_threshold_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_shipping_threshold_with_http_info(shipping_threshold_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingThreshold>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->create_shipping_threshold_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipping_threshold_create** | [**ShippingThresholdCreate**](ShippingThresholdCreate.md) |  |  |

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_shipping_threshold

> delete_shipping_threshold(threshold_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingThresholdApi.new
threshold_id = 'threshold_id_example' # String | 

begin
  
  api_instance.delete_shipping_threshold(threshold_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->delete_shipping_threshold: #{e}"
end
```

#### Using the delete_shipping_threshold_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_shipping_threshold_with_http_info(threshold_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_shipping_threshold_with_http_info(threshold_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->delete_shipping_threshold_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **threshold_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_deliverable

> <DeliverableResponse> get_deliverable(product_id, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingThresholdApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
opts = {
  warehouse_id: 'warehouse_id_example' # String | 
}

begin
  
  result = api_instance.get_deliverable(product_id, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->get_deliverable: #{e}"
end
```

#### Using the get_deliverable_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliverableResponse>, Integer, Hash)> get_deliverable_with_http_info(product_id, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_deliverable_with_http_info(product_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliverableResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->get_deliverable_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **warehouse_id** | **String** |  | [optional] |

### Return type

[**DeliverableResponse**](DeliverableResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_shipping_threshold

> <ShippingThreshold> get_shipping_threshold(threshold_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingThresholdApi.new
threshold_id = 'threshold_id_example' # String | 

begin
  
  result = api_instance.get_shipping_threshold(threshold_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->get_shipping_threshold: #{e}"
end
```

#### Using the get_shipping_threshold_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingThreshold>, Integer, Hash)> get_shipping_threshold_with_http_info(threshold_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_shipping_threshold_with_http_info(threshold_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingThreshold>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->get_shipping_threshold_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **threshold_id** | **String** |  |  |

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_shipping_thresholds

> <Array<ShippingThreshold>> list_shipping_thresholds(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingThresholdApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  product_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  warehouse_id: 'warehouse_id_example', # String | 
  is_active: true # Boolean | 
}

begin
  
  result = api_instance.list_shipping_thresholds(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->list_shipping_thresholds: #{e}"
end
```

#### Using the list_shipping_thresholds_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ShippingThreshold>>, Integer, Hash)> list_shipping_thresholds_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_shipping_thresholds_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ShippingThreshold>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->list_shipping_thresholds_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **warehouse_id** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |

### Return type

[**Array&lt;ShippingThreshold&gt;**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_shipping_threshold

> <ShippingThreshold> update_shipping_threshold(threshold_id, shipping_threshold_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingThresholdApi.new
threshold_id = 'threshold_id_example' # String | 
shipping_threshold_update = SimplebillyApi::ShippingThresholdUpdate.new # ShippingThresholdUpdate | 

begin
  
  result = api_instance.update_shipping_threshold(threshold_id, shipping_threshold_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->update_shipping_threshold: #{e}"
end
```

#### Using the update_shipping_threshold_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingThreshold>, Integer, Hash)> update_shipping_threshold_with_http_info(threshold_id, shipping_threshold_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_shipping_threshold_with_http_info(threshold_id, shipping_threshold_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingThreshold>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingThresholdApi->update_shipping_threshold_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **threshold_id** | **String** |  |  |
| **shipping_threshold_update** | [**ShippingThresholdUpdate**](ShippingThresholdUpdate.md) |  |  |

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

