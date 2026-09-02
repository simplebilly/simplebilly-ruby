# SimplebillyApi::DeliveryDateApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_delivery_date**](DeliveryDateApi.md#create_delivery_date) | **POST** /api/v1/delivery-dates |  |
| [**delete_delivery_date**](DeliveryDateApi.md#delete_delivery_date) | **DELETE** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**get_delivery_date**](DeliveryDateApi.md#get_delivery_date) | **GET** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**get_delivery_performance**](DeliveryDateApi.md#get_delivery_performance) | **GET** /api/v1/delivery-dates/performance | On-time performance summary: how many promised delivery dates were met within a period. |
| [**list_delivery_dates**](DeliveryDateApi.md#list_delivery_dates) | **GET** /api/v1/delivery-dates/ |  |
| [**update_delivery_date**](DeliveryDateApi.md#update_delivery_date) | **PUT** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**update_delivery_date_status**](DeliveryDateApi.md#update_delivery_date_status) | **PUT** /api/v1/delivery-dates/{delivery_date_id}/status |  |


## create_delivery_date

> <DeliveryDate> create_delivery_date(delivery_date_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryDateApi.new
delivery_date_create = SimplebillyApi::DeliveryDateCreate.new({order_number: 'order_number_example', promised_date: Date.today, status: SimplebillyApi::DeliveryDateStatus::PROMISED}) # DeliveryDateCreate | 

begin
  
  result = api_instance.create_delivery_date(delivery_date_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->create_delivery_date: #{e}"
end
```

#### Using the create_delivery_date_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryDate>, Integer, Hash)> create_delivery_date_with_http_info(delivery_date_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_delivery_date_with_http_info(delivery_date_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryDate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->create_delivery_date_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_date_create** | [**DeliveryDateCreate**](DeliveryDateCreate.md) |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_delivery_date

> delete_delivery_date(delivery_date_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryDateApi.new
delivery_date_id = 'delivery_date_id_example' # String | 

begin
  
  api_instance.delete_delivery_date(delivery_date_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->delete_delivery_date: #{e}"
end
```

#### Using the delete_delivery_date_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_delivery_date_with_http_info(delivery_date_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_delivery_date_with_http_info(delivery_date_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->delete_delivery_date_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_date_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_delivery_date

> <DeliveryDate> get_delivery_date(delivery_date_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryDateApi.new
delivery_date_id = 'delivery_date_id_example' # String | 

begin
  
  result = api_instance.get_delivery_date(delivery_date_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->get_delivery_date: #{e}"
end
```

#### Using the get_delivery_date_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryDate>, Integer, Hash)> get_delivery_date_with_http_info(delivery_date_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_delivery_date_with_http_info(delivery_date_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryDate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->get_delivery_date_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_date_id** | **String** |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_delivery_performance

> Object get_delivery_performance(opts)

On-time performance summary: how many promised delivery dates were met within a period.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryDateApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  order_number: 'order_number_example', # String | 
  status: 'status_example', # String | 
  from: Date.parse('2013-10-20'), # Date | Only dates on or after this date.
  to: Date.parse('2013-10-20') # Date | Only dates on or before this date.
}

begin
  # On-time performance summary: how many promised delivery dates were met within a period.
  result = api_instance.get_delivery_performance(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->get_delivery_performance: #{e}"
end
```

#### Using the get_delivery_performance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> get_delivery_performance_with_http_info(opts)

```ruby
begin
  # On-time performance summary: how many promised delivery dates were met within a period.
  data, status_code, headers = api_instance.get_delivery_performance_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->get_delivery_performance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **order_number** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **from** | **Date** | Only dates on or after this date. | [optional] |
| **to** | **Date** | Only dates on or before this date. | [optional] |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_delivery_dates

> <Array<DeliveryDate>> list_delivery_dates(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryDateApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  order_number: 'order_number_example', # String | 
  status: 'status_example', # String | 
  from: Date.parse('2013-10-20'), # Date | Only dates on or after this date.
  to: Date.parse('2013-10-20') # Date | Only dates on or before this date.
}

begin
  
  result = api_instance.list_delivery_dates(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->list_delivery_dates: #{e}"
end
```

#### Using the list_delivery_dates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<DeliveryDate>>, Integer, Hash)> list_delivery_dates_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_delivery_dates_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<DeliveryDate>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->list_delivery_dates_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **order_number** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **from** | **Date** | Only dates on or after this date. | [optional] |
| **to** | **Date** | Only dates on or before this date. | [optional] |

### Return type

[**Array&lt;DeliveryDate&gt;**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_delivery_date

> <DeliveryDate> update_delivery_date(delivery_date_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryDateApi.new
delivery_date_id = 'delivery_date_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_delivery_date(delivery_date_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->update_delivery_date: #{e}"
end
```

#### Using the update_delivery_date_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryDate>, Integer, Hash)> update_delivery_date_with_http_info(delivery_date_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_delivery_date_with_http_info(delivery_date_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryDate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->update_delivery_date_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_date_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_delivery_date_status

> <DeliveryDate> update_delivery_date_status(delivery_date_id, delivery_date_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryDateApi.new
delivery_date_id = 'delivery_date_id_example' # String | 
delivery_date_status_update = SimplebillyApi::DeliveryDateStatusUpdate.new({status: 'status_example'}) # DeliveryDateStatusUpdate | 

begin
  
  result = api_instance.update_delivery_date_status(delivery_date_id, delivery_date_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->update_delivery_date_status: #{e}"
end
```

#### Using the update_delivery_date_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryDate>, Integer, Hash)> update_delivery_date_status_with_http_info(delivery_date_id, delivery_date_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_delivery_date_status_with_http_info(delivery_date_id, delivery_date_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryDate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryDateApi->update_delivery_date_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_date_id** | **String** |  |  |
| **delivery_date_status_update** | [**DeliveryDateStatusUpdate**](DeliveryDateStatusUpdate.md) |  |  |

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

