# SimplebillyApi::ParticipationApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_participation**](ParticipationApi.md#create_participation) | **POST** /api/v1/participations |  |
| [**delete_participation**](ParticipationApi.md#delete_participation) | **DELETE** /api/v1/participations/{id} |  |
| [**get_participation**](ParticipationApi.md#get_participation) | **GET** /api/v1/participations/{id} |  |
| [**get_participations**](ParticipationApi.md#get_participations) | **GET** /api/v1/participations/ |  |
| [**update_participation**](ParticipationApi.md#update_participation) | **PUT** /api/v1/participations/{id} |  |


## create_participation

> <Participation> create_participation(participation_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ParticipationApi.new
participation_create = SimplebillyApi::ParticipationCreate.new # ParticipationCreate | 

begin
  
  result = api_instance.create_participation(participation_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->create_participation: #{e}"
end
```

#### Using the create_participation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Participation>, Integer, Hash)> create_participation_with_http_info(participation_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_participation_with_http_info(participation_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Participation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->create_participation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **participation_create** | [**ParticipationCreate**](ParticipationCreate.md) |  |  |

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_participation

> delete_participation(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ParticipationApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_participation(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->delete_participation: #{e}"
end
```

#### Using the delete_participation_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_participation_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_participation_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->delete_participation_with_http_info: #{e}"
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


## get_participation

> <Participation> get_participation(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ParticipationApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_participation(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->get_participation: #{e}"
end
```

#### Using the get_participation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Participation>, Integer, Hash)> get_participation_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_participation_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Participation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->get_participation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_participations

> <Array<Participation>> get_participations(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ParticipationApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_participations(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->get_participations: #{e}"
end
```

#### Using the get_participations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Participation>>, Integer, Hash)> get_participations_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_participations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Participation>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->get_participations_with_http_info: #{e}"
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

[**Array&lt;Participation&gt;**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_participation

> <Participation> update_participation(id, participation_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ParticipationApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
participation_update = SimplebillyApi::ParticipationUpdate.new # ParticipationUpdate | 

begin
  
  result = api_instance.update_participation(id, participation_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->update_participation: #{e}"
end
```

#### Using the update_participation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Participation>, Integer, Hash)> update_participation_with_http_info(id, participation_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_participation_with_http_info(id, participation_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Participation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ParticipationApi->update_participation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **participation_update** | [**ParticipationUpdate**](ParticipationUpdate.md) |  |  |

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

