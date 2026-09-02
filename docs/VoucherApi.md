# SimplebillyApi::VoucherApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_voucher**](VoucherApi.md#create_voucher) | **POST** /api/v1/vouchers |  |
| [**delete_voucher**](VoucherApi.md#delete_voucher) | **DELETE** /api/v1/vouchers/{voucher_id} |  |
| [**get_voucher**](VoucherApi.md#get_voucher) | **GET** /api/v1/vouchers/{voucher_id} |  |
| [**list_vouchers**](VoucherApi.md#list_vouchers) | **GET** /api/v1/vouchers/ |  |
| [**update_voucher**](VoucherApi.md#update_voucher) | **PUT** /api/v1/vouchers/{voucher_id} |  |
| [**voucher_restore**](VoucherApi.md#voucher_restore) | **POST** /api/v1/vouchers/{voucher_id}/restore |  |


## create_voucher

> <Voucher> create_voucher(voucher_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::VoucherApi.new
voucher_create = SimplebillyApi::VoucherCreate.new({currency: 'currency_example', voucher_date: Date.today, voucher_status: SimplebillyApi::VoucherStatus::OPEN, voucher_type: SimplebillyApi::VoucherType::INVOICE}) # VoucherCreate | 

begin
  
  result = api_instance.create_voucher(voucher_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->create_voucher: #{e}"
end
```

#### Using the create_voucher_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Voucher>, Integer, Hash)> create_voucher_with_http_info(voucher_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_voucher_with_http_info(voucher_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Voucher>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->create_voucher_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **voucher_create** | [**VoucherCreate**](VoucherCreate.md) |  |  |

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_voucher

> delete_voucher(voucher_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::VoucherApi.new
voucher_id = 'voucher_id_example' # String | 

begin
  
  api_instance.delete_voucher(voucher_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->delete_voucher: #{e}"
end
```

#### Using the delete_voucher_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_voucher_with_http_info(voucher_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_voucher_with_http_info(voucher_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->delete_voucher_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **voucher_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_voucher

> <Voucher> get_voucher(voucher_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::VoucherApi.new
voucher_id = 'voucher_id_example' # String | 

begin
  
  result = api_instance.get_voucher(voucher_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->get_voucher: #{e}"
end
```

#### Using the get_voucher_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Voucher>, Integer, Hash)> get_voucher_with_http_info(voucher_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_voucher_with_http_info(voucher_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Voucher>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->get_voucher_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **voucher_id** | **String** |  |  |

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_vouchers

> <Array<Voucher>> list_vouchers(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::VoucherApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  voucher_type: 'voucher_type_example', # String | 
  voucher_status: 'voucher_status_example', # String | 
  contact_name: 'contact_name_example', # String | 
  date_from: Date.parse('2013-10-20'), # Date | 
  date_to: Date.parse('2013-10-20') # Date | 
}

begin
  
  result = api_instance.list_vouchers(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->list_vouchers: #{e}"
end
```

#### Using the list_vouchers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Voucher>>, Integer, Hash)> list_vouchers_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_vouchers_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Voucher>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->list_vouchers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **voucher_type** | **String** |  | [optional] |
| **voucher_status** | **String** |  | [optional] |
| **contact_name** | **String** |  | [optional] |
| **date_from** | **Date** |  | [optional] |
| **date_to** | **Date** |  | [optional] |

### Return type

[**Array&lt;Voucher&gt;**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_voucher

> <Voucher> update_voucher(voucher_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::VoucherApi.new
voucher_id = 'voucher_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_voucher(voucher_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->update_voucher: #{e}"
end
```

#### Using the update_voucher_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Voucher>, Integer, Hash)> update_voucher_with_http_info(voucher_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_voucher_with_http_info(voucher_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Voucher>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->update_voucher_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **voucher_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## voucher_restore

> <Voucher> voucher_restore(voucher_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::VoucherApi.new
voucher_id = 'voucher_id_example' # String | 

begin
  
  result = api_instance.voucher_restore(voucher_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->voucher_restore: #{e}"
end
```

#### Using the voucher_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Voucher>, Integer, Hash)> voucher_restore_with_http_info(voucher_id)

```ruby
begin
  
  data, status_code, headers = api_instance.voucher_restore_with_http_info(voucher_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Voucher>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling VoucherApi->voucher_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **voucher_id** | **String** |  |  |

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

