# SimplebillyApi::DeliveryAppointmentApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_delivery_appointment**](DeliveryAppointmentApi.md#create_delivery_appointment) | **POST** /api/v1/delivery-appointments |  |
| [**delete_delivery_appointment**](DeliveryAppointmentApi.md#delete_delivery_appointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} |  |
| [**get_delivery_appointment**](DeliveryAppointmentApi.md#get_delivery_appointment) | **GET** /api/v1/delivery-appointments/{appointment_id} |  |
| [**get_public_delivery_appointment_status**](DeliveryAppointmentApi.md#get_public_delivery_appointment_status) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match. |
| [**list_delivery_appointments**](DeliveryAppointmentApi.md#list_delivery_appointments) | **GET** /api/v1/delivery-appointments |  |
| [**request_public_delivery_appointment**](DeliveryAppointmentApi.md#request_public_delivery_appointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request. |
| [**update_delivery_appointment**](DeliveryAppointmentApi.md#update_delivery_appointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} |  |
| [**update_delivery_appointment_status**](DeliveryAppointmentApi.md#update_delivery_appointment_status) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status |  |


## create_delivery_appointment

> <DeliveryAppointment> create_delivery_appointment(delivery_appointment_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
delivery_appointment_create = SimplebillyApi::DeliveryAppointmentCreate.new({email: 'email_example', requested_date: Date.today, status: SimplebillyApi::DeliveryAppointmentStatus::REQUESTED, supplier_name: 'supplier_name_example', warehouse_id: 'warehouse_id_example'}) # DeliveryAppointmentCreate | 

begin
  
  result = api_instance.create_delivery_appointment(delivery_appointment_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->create_delivery_appointment: #{e}"
end
```

#### Using the create_delivery_appointment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryAppointment>, Integer, Hash)> create_delivery_appointment_with_http_info(delivery_appointment_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_delivery_appointment_with_http_info(delivery_appointment_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryAppointment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->create_delivery_appointment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_appointment_create** | [**DeliveryAppointmentCreate**](DeliveryAppointmentCreate.md) |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_delivery_appointment

> delete_delivery_appointment(appointment_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
appointment_id = 'appointment_id_example' # String | 

begin
  
  api_instance.delete_delivery_appointment(appointment_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->delete_delivery_appointment: #{e}"
end
```

#### Using the delete_delivery_appointment_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_delivery_appointment_with_http_info(appointment_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_delivery_appointment_with_http_info(appointment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->delete_delivery_appointment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **appointment_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_delivery_appointment

> <DeliveryAppointment> get_delivery_appointment(appointment_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
appointment_id = 'appointment_id_example' # String | 

begin
  
  result = api_instance.get_delivery_appointment(appointment_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->get_delivery_appointment: #{e}"
end
```

#### Using the get_delivery_appointment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryAppointment>, Integer, Hash)> get_delivery_appointment_with_http_info(appointment_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_delivery_appointment_with_http_info(appointment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryAppointment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->get_delivery_appointment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **appointment_id** | **String** |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_public_delivery_appointment_status

> <PublicDeliveryAppointmentStatusResponse> get_public_delivery_appointment_status(appointment_id, email, token)

Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
appointment_id = 'appointment_id_example' # String | 
email = 'email_example' # String | 
token = 'token_example' # String | 

begin
  # Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
  result = api_instance.get_public_delivery_appointment_status(appointment_id, email, token)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->get_public_delivery_appointment_status: #{e}"
end
```

#### Using the get_public_delivery_appointment_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicDeliveryAppointmentStatusResponse>, Integer, Hash)> get_public_delivery_appointment_status_with_http_info(appointment_id, email, token)

```ruby
begin
  # Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
  data, status_code, headers = api_instance.get_public_delivery_appointment_status_with_http_info(appointment_id, email, token)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicDeliveryAppointmentStatusResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->get_public_delivery_appointment_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **appointment_id** | **String** |  |  |
| **email** | **String** |  |  |
| **token** | **String** |  |  |

### Return type

[**PublicDeliveryAppointmentStatusResponse**](PublicDeliveryAppointmentStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_delivery_appointments

> <Array<DeliveryAppointment>> list_delivery_appointments(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  warehouse_id: 'warehouse_id_example', # String | 
  from: Date.parse('2013-10-20'), # Date | 
  to: Date.parse('2013-10-20') # Date | 
}

begin
  
  result = api_instance.list_delivery_appointments(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->list_delivery_appointments: #{e}"
end
```

#### Using the list_delivery_appointments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<DeliveryAppointment>>, Integer, Hash)> list_delivery_appointments_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_delivery_appointments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<DeliveryAppointment>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->list_delivery_appointments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **warehouse_id** | **String** |  | [optional] |
| **from** | **Date** |  | [optional] |
| **to** | **Date** |  | [optional] |

### Return type

[**Array&lt;DeliveryAppointment&gt;**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## request_public_delivery_appointment

> <PublicDeliveryAppointmentResponse> request_public_delivery_appointment(public_delivery_appointment_request)

Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
public_delivery_appointment_request = SimplebillyApi::PublicDeliveryAppointmentRequest.new({email: 'email_example', requested_date: Date.today, supplier_name: 'supplier_name_example', warehouse_code: 'warehouse_code_example'}) # PublicDeliveryAppointmentRequest | 

begin
  # Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.
  result = api_instance.request_public_delivery_appointment(public_delivery_appointment_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->request_public_delivery_appointment: #{e}"
end
```

#### Using the request_public_delivery_appointment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicDeliveryAppointmentResponse>, Integer, Hash)> request_public_delivery_appointment_with_http_info(public_delivery_appointment_request)

```ruby
begin
  # Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.
  data, status_code, headers = api_instance.request_public_delivery_appointment_with_http_info(public_delivery_appointment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicDeliveryAppointmentResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->request_public_delivery_appointment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **public_delivery_appointment_request** | [**PublicDeliveryAppointmentRequest**](PublicDeliveryAppointmentRequest.md) |  |  |

### Return type

[**PublicDeliveryAppointmentResponse**](PublicDeliveryAppointmentResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_delivery_appointment

> <DeliveryAppointment> update_delivery_appointment(appointment_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
appointment_id = 'appointment_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_delivery_appointment(appointment_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->update_delivery_appointment: #{e}"
end
```

#### Using the update_delivery_appointment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryAppointment>, Integer, Hash)> update_delivery_appointment_with_http_info(appointment_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_delivery_appointment_with_http_info(appointment_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryAppointment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->update_delivery_appointment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **appointment_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_delivery_appointment_status

> <DeliveryAppointment> update_delivery_appointment_status(appointment_id, appointment_status_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::DeliveryAppointmentApi.new
appointment_id = 'appointment_id_example' # String | 
appointment_status_update = SimplebillyApi::AppointmentStatusUpdate.new({status: 'status_example'}) # AppointmentStatusUpdate | 

begin
  
  result = api_instance.update_delivery_appointment_status(appointment_id, appointment_status_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->update_delivery_appointment_status: #{e}"
end
```

#### Using the update_delivery_appointment_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryAppointment>, Integer, Hash)> update_delivery_appointment_status_with_http_info(appointment_id, appointment_status_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_delivery_appointment_status_with_http_info(appointment_id, appointment_status_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryAppointment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling DeliveryAppointmentApi->update_delivery_appointment_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **appointment_id** | **String** |  |  |
| **appointment_status_update** | [**AppointmentStatusUpdate**](AppointmentStatusUpdate.md) |  |  |

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

