# SimplebillyApi::KycRecordApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_kyc_record**](KycRecordApi.md#create_kyc_record) | **POST** /api/v1/kyc-records |  |
| [**delete_kyc_record**](KycRecordApi.md#delete_kyc_record) | **DELETE** /api/v1/kyc-records/{id} |  |
| [**get_kyc_record**](KycRecordApi.md#get_kyc_record) | **GET** /api/v1/kyc-records/{id} |  |
| [**get_kyc_records**](KycRecordApi.md#get_kyc_records) | **GET** /api/v1/kyc-records/ |  |
| [**update_kyc_record**](KycRecordApi.md#update_kyc_record) | **PUT** /api/v1/kyc-records/{id} |  |


## create_kyc_record

> <KycRecord> create_kyc_record(kyc_record_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KycRecordApi.new
kyc_record_create = SimplebillyApi::KycRecordCreate.new # KycRecordCreate | 

begin
  
  result = api_instance.create_kyc_record(kyc_record_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->create_kyc_record: #{e}"
end
```

#### Using the create_kyc_record_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KycRecord>, Integer, Hash)> create_kyc_record_with_http_info(kyc_record_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_kyc_record_with_http_info(kyc_record_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KycRecord>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->create_kyc_record_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **kyc_record_create** | [**KycRecordCreate**](KycRecordCreate.md) |  |  |

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_kyc_record

> delete_kyc_record(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KycRecordApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_kyc_record(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->delete_kyc_record: #{e}"
end
```

#### Using the delete_kyc_record_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_kyc_record_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_kyc_record_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->delete_kyc_record_with_http_info: #{e}"
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


## get_kyc_record

> <KycRecord> get_kyc_record(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KycRecordApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_kyc_record(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->get_kyc_record: #{e}"
end
```

#### Using the get_kyc_record_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KycRecord>, Integer, Hash)> get_kyc_record_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_kyc_record_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KycRecord>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->get_kyc_record_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_kyc_records

> <Array<KycRecord>> get_kyc_records(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KycRecordApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_kyc_records(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->get_kyc_records: #{e}"
end
```

#### Using the get_kyc_records_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<KycRecord>>, Integer, Hash)> get_kyc_records_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_kyc_records_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<KycRecord>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->get_kyc_records_with_http_info: #{e}"
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

[**Array&lt;KycRecord&gt;**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_kyc_record

> <KycRecord> update_kyc_record(id, kyc_record_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::KycRecordApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
kyc_record_update = SimplebillyApi::KycRecordUpdate.new # KycRecordUpdate | 

begin
  
  result = api_instance.update_kyc_record(id, kyc_record_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->update_kyc_record: #{e}"
end
```

#### Using the update_kyc_record_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KycRecord>, Integer, Hash)> update_kyc_record_with_http_info(id, kyc_record_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_kyc_record_with_http_info(id, kyc_record_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KycRecord>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling KycRecordApi->update_kyc_record_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **kyc_record_update** | [**KycRecordUpdate**](KycRecordUpdate.md) |  |  |

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

