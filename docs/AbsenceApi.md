# SimplebillyApi::AbsenceApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_absence**](AbsenceApi.md#create_absence) | **POST** /api/v1/absences |  |
| [**delete_absence**](AbsenceApi.md#delete_absence) | **DELETE** /api/v1/absences/{id} |  |
| [**get_absence**](AbsenceApi.md#get_absence) | **GET** /api/v1/absences/{id} |  |
| [**get_absences**](AbsenceApi.md#get_absences) | **GET** /api/v1/absences/ |  |
| [**update_absence**](AbsenceApi.md#update_absence) | **PUT** /api/v1/absences/{id} |  |


## create_absence

> <Absence> create_absence(absence_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AbsenceApi.new
absence_create = SimplebillyApi::AbsenceCreate.new # AbsenceCreate | 

begin
  
  result = api_instance.create_absence(absence_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->create_absence: #{e}"
end
```

#### Using the create_absence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Absence>, Integer, Hash)> create_absence_with_http_info(absence_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_absence_with_http_info(absence_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Absence>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->create_absence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **absence_create** | [**AbsenceCreate**](AbsenceCreate.md) |  |  |

### Return type

[**Absence**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_absence

> delete_absence(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AbsenceApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_absence(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->delete_absence: #{e}"
end
```

#### Using the delete_absence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_absence_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_absence_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->delete_absence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_absence

> <Absence> get_absence(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AbsenceApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_absence(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->get_absence: #{e}"
end
```

#### Using the get_absence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Absence>, Integer, Hash)> get_absence_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_absence_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Absence>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->get_absence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Absence**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_absences

> <Array<Absence>> get_absences(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AbsenceApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_absences(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->get_absences: #{e}"
end
```

#### Using the get_absences_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Absence>>, Integer, Hash)> get_absences_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_absences_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Absence>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->get_absences_with_http_info: #{e}"
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

[**Array&lt;Absence&gt;**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_absence

> <Absence> update_absence(id, absence_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AbsenceApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
absence_update = SimplebillyApi::AbsenceUpdate.new # AbsenceUpdate | 

begin
  
  result = api_instance.update_absence(id, absence_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->update_absence: #{e}"
end
```

#### Using the update_absence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Absence>, Integer, Hash)> update_absence_with_http_info(id, absence_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_absence_with_http_info(id, absence_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Absence>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AbsenceApi->update_absence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **absence_update** | [**AbsenceUpdate**](AbsenceUpdate.md) |  |  |

### Return type

[**Absence**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

