# SimplebillyApi::SilentPartnerApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_silent_partner**](SilentPartnerApi.md#create_silent_partner) | **POST** /api/v1/silent-partners |  |
| [**delete_silent_partner**](SilentPartnerApi.md#delete_silent_partner) | **DELETE** /api/v1/silent-partners/{id} |  |
| [**get_silent_partner**](SilentPartnerApi.md#get_silent_partner) | **GET** /api/v1/silent-partners/{id} |  |
| [**get_silent_partners**](SilentPartnerApi.md#get_silent_partners) | **GET** /api/v1/silent-partners/ |  |
| [**update_silent_partner**](SilentPartnerApi.md#update_silent_partner) | **PUT** /api/v1/silent-partners/{id} |  |


## create_silent_partner

> <SilentPartner> create_silent_partner(silent_partner_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SilentPartnerApi.new
silent_partner_create = SimplebillyApi::SilentPartnerCreate.new({instrument_type: SimplebillyApi::InstrumentType::TYPISCH}) # SilentPartnerCreate | 

begin
  
  result = api_instance.create_silent_partner(silent_partner_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->create_silent_partner: #{e}"
end
```

#### Using the create_silent_partner_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SilentPartner>, Integer, Hash)> create_silent_partner_with_http_info(silent_partner_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_silent_partner_with_http_info(silent_partner_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SilentPartner>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->create_silent_partner_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **silent_partner_create** | [**SilentPartnerCreate**](SilentPartnerCreate.md) |  |  |

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_silent_partner

> delete_silent_partner(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SilentPartnerApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_silent_partner(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->delete_silent_partner: #{e}"
end
```

#### Using the delete_silent_partner_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_silent_partner_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_silent_partner_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->delete_silent_partner_with_http_info: #{e}"
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


## get_silent_partner

> <SilentPartner> get_silent_partner(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SilentPartnerApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_silent_partner(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->get_silent_partner: #{e}"
end
```

#### Using the get_silent_partner_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SilentPartner>, Integer, Hash)> get_silent_partner_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_silent_partner_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SilentPartner>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->get_silent_partner_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_silent_partners

> <Array<SilentPartner>> get_silent_partners(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SilentPartnerApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_silent_partners(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->get_silent_partners: #{e}"
end
```

#### Using the get_silent_partners_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<SilentPartner>>, Integer, Hash)> get_silent_partners_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_silent_partners_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<SilentPartner>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->get_silent_partners_with_http_info: #{e}"
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

[**Array&lt;SilentPartner&gt;**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_silent_partner

> <SilentPartner> update_silent_partner(id, silent_partner_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SilentPartnerApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
silent_partner_update = SimplebillyApi::SilentPartnerUpdate.new # SilentPartnerUpdate | 

begin
  
  result = api_instance.update_silent_partner(id, silent_partner_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->update_silent_partner: #{e}"
end
```

#### Using the update_silent_partner_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SilentPartner>, Integer, Hash)> update_silent_partner_with_http_info(id, silent_partner_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_silent_partner_with_http_info(id, silent_partner_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SilentPartner>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SilentPartnerApi->update_silent_partner_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **silent_partner_update** | [**SilentPartnerUpdate**](SilentPartnerUpdate.md) |  |  |

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

