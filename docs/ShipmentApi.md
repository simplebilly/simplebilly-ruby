# SimplebillyApi::ShipmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_shipment**](ShipmentApi.md#create_shipment) | **POST** /api/v1/shipments |  |
| [**create_shipment_from_order**](ShipmentApi.md#create_shipment_from_order) | **POST** /api/v1/orders/{order_number}/shipments | Create a real shipment for an order: calls the configured carrier&#39;s label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped. |
| [**delete_shipment**](ShipmentApi.md#delete_shipment) | **DELETE** /api/v1/shipments/{shipment_id} |  |
| [**get_shipment**](ShipmentApi.md#get_shipment) | **GET** /api/v1/shipments/{shipment_id} |  |
| [**list_shipments**](ShipmentApi.md#list_shipments) | **GET** /api/v1/shipments |  |
| [**track_order_public**](ShipmentApi.md#track_order_public) | **POST** /api/v1/public/track | Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API). |
| [**track_shipment_api**](ShipmentApi.md#track_shipment_api) | **GET** /api/v1/shipments/{shipment_id}/tracking |  |
| [**update_shipment_status**](ShipmentApi.md#update_shipment_status) | **PUT** /api/v1/shipments/{shipment_id}/status |  |


## create_shipment

> <Shipment> create_shipment(shipment)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
shipment = SimplebillyApi::Shipment.new({order_id: 'order_id_example', shipment_date: Date.today, shipping_carrier: 'shipping_carrier_example', status: 'status_example'}) # Shipment | 

begin
  
  result = api_instance.create_shipment(shipment)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->create_shipment: #{e}"
end
```

#### Using the create_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Shipment>, Integer, Hash)> create_shipment_with_http_info(shipment)

```ruby
begin
  
  data, status_code, headers = api_instance.create_shipment_with_http_info(shipment)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Shipment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->create_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment** | [**Shipment**](Shipment.md) |  |  |

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_shipment_from_order

> <Shipment> create_shipment_from_order(order_number, create_shipment_request)

Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
order_number = 'order_number_example' # String | 
create_shipment_request = SimplebillyApi::CreateShipmentRequest.new({carrier: 'carrier_example'}) # CreateShipmentRequest | 

begin
  # Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
  result = api_instance.create_shipment_from_order(order_number, create_shipment_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->create_shipment_from_order: #{e}"
end
```

#### Using the create_shipment_from_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Shipment>, Integer, Hash)> create_shipment_from_order_with_http_info(order_number, create_shipment_request)

```ruby
begin
  # Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
  data, status_code, headers = api_instance.create_shipment_from_order_with_http_info(order_number, create_shipment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Shipment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->create_shipment_from_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |
| **create_shipment_request** | [**CreateShipmentRequest**](CreateShipmentRequest.md) |  |  |

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_shipment

> delete_shipment(shipment_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
shipment_id = 'shipment_id_example' # String | 

begin
  
  api_instance.delete_shipment(shipment_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->delete_shipment: #{e}"
end
```

#### Using the delete_shipment_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_shipment_with_http_info(shipment_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_shipment_with_http_info(shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->delete_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_shipment

> <Shipment> get_shipment(shipment_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
shipment_id = 'shipment_id_example' # String | 

begin
  
  result = api_instance.get_shipment(shipment_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->get_shipment: #{e}"
end
```

#### Using the get_shipment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Shipment>, Integer, Hash)> get_shipment_with_http_info(shipment_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_shipment_with_http_info(shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Shipment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->get_shipment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment_id** | **String** |  |  |

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_shipments

> <Array<Shipment>> list_shipments(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.list_shipments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->list_shipments: #{e}"
end
```

#### Using the list_shipments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Shipment>>, Integer, Hash)> list_shipments_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_shipments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Shipment>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->list_shipments_with_http_info: #{e}"
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

[**Array&lt;Shipment&gt;**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## track_order_public

> <TrackOrderResponse> track_order_public(track_order_request)

Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
track_order_request = SimplebillyApi::TrackOrderRequest.new({email: 'email_example', order_number: 'order_number_example'}) # TrackOrderRequest | 

begin
  # Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
  result = api_instance.track_order_public(track_order_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->track_order_public: #{e}"
end
```

#### Using the track_order_public_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TrackOrderResponse>, Integer, Hash)> track_order_public_with_http_info(track_order_request)

```ruby
begin
  # Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
  data, status_code, headers = api_instance.track_order_public_with_http_info(track_order_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TrackOrderResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->track_order_public_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **track_order_request** | [**TrackOrderRequest**](TrackOrderRequest.md) |  |  |

### Return type

[**TrackOrderResponse**](TrackOrderResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## track_shipment_api

> <TrackingInfo> track_shipment_api(shipment_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
shipment_id = 'shipment_id_example' # String | 

begin
  
  result = api_instance.track_shipment_api(shipment_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->track_shipment_api: #{e}"
end
```

#### Using the track_shipment_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TrackingInfo>, Integer, Hash)> track_shipment_api_with_http_info(shipment_id)

```ruby
begin
  
  data, status_code, headers = api_instance.track_shipment_api_with_http_info(shipment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TrackingInfo>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->track_shipment_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment_id** | **String** |  |  |

### Return type

[**TrackingInfo**](TrackingInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_shipment_status

> <Shipment> update_shipment_status(shipment_id, shipment_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShipmentApi.new
shipment_id = 'shipment_id_example' # String | 
shipment_status_update = SimplebillyApi::ShipmentStatusUpdate.new({status: 'status_example'}) # ShipmentStatusUpdate | 

begin
  
  result = api_instance.update_shipment_status(shipment_id, shipment_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->update_shipment_status: #{e}"
end
```

#### Using the update_shipment_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Shipment>, Integer, Hash)> update_shipment_status_with_http_info(shipment_id, shipment_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_shipment_status_with_http_info(shipment_id, shipment_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Shipment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShipmentApi->update_shipment_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment_id** | **String** |  |  |
| **shipment_status_update** | [**ShipmentStatusUpdate**](ShipmentStatusUpdate.md) |  |  |

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

