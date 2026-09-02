# SimplebillyApi::CouponApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**coupon_restore**](CouponApi.md#coupon_restore) | **POST** /api/v1/coupons/{coupon_id}/restore |  |
| [**create_coupon**](CouponApi.md#create_coupon) | **POST** /api/v1/coupons |  |
| [**delete_coupon**](CouponApi.md#delete_coupon) | **DELETE** /api/v1/coupons/{coupon_id} |  |
| [**get_coupon**](CouponApi.md#get_coupon) | **GET** /api/v1/coupons/{coupon_id} |  |
| [**list_coupons**](CouponApi.md#list_coupons) | **GET** /api/v1/coupons/ |  |
| [**update_coupon**](CouponApi.md#update_coupon) | **PUT** /api/v1/coupons/{coupon_id} |  |


## coupon_restore

> <Coupon> coupon_restore(coupon_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CouponApi.new
coupon_id = 'coupon_id_example' # String | 

begin
  
  result = api_instance.coupon_restore(coupon_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->coupon_restore: #{e}"
end
```

#### Using the coupon_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Coupon>, Integer, Hash)> coupon_restore_with_http_info(coupon_id)

```ruby
begin
  
  data, status_code, headers = api_instance.coupon_restore_with_http_info(coupon_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Coupon>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->coupon_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **coupon_id** | **String** |  |  |

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_coupon

> <Coupon> create_coupon(coupon_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CouponApi.new
coupon_create = SimplebillyApi::CouponCreate.new({code: 'code_example', discount_type: SimplebillyApi::DiscountType::PERCENTAGE, discount_value: 'discount_value_example'}) # CouponCreate | 

begin
  
  result = api_instance.create_coupon(coupon_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->create_coupon: #{e}"
end
```

#### Using the create_coupon_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Coupon>, Integer, Hash)> create_coupon_with_http_info(coupon_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_coupon_with_http_info(coupon_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Coupon>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->create_coupon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **coupon_create** | [**CouponCreate**](CouponCreate.md) |  |  |

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_coupon

> delete_coupon(coupon_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CouponApi.new
coupon_id = 'coupon_id_example' # String | 

begin
  
  api_instance.delete_coupon(coupon_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->delete_coupon: #{e}"
end
```

#### Using the delete_coupon_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_coupon_with_http_info(coupon_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_coupon_with_http_info(coupon_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->delete_coupon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **coupon_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_coupon

> <Coupon> get_coupon(coupon_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CouponApi.new
coupon_id = 'coupon_id_example' # String | 

begin
  
  result = api_instance.get_coupon(coupon_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->get_coupon: #{e}"
end
```

#### Using the get_coupon_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Coupon>, Integer, Hash)> get_coupon_with_http_info(coupon_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_coupon_with_http_info(coupon_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Coupon>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->get_coupon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **coupon_id** | **String** |  |  |

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_coupons

> <Array<Coupon>> list_coupons(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CouponApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  is_active: true, # Boolean | 
  code: 'code_example', # String | 
  discount_type: 'discount_type_example' # String | 
}

begin
  
  result = api_instance.list_coupons(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->list_coupons: #{e}"
end
```

#### Using the list_coupons_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Coupon>>, Integer, Hash)> list_coupons_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_coupons_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Coupon>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->list_coupons_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **code** | **String** |  | [optional] |
| **discount_type** | **String** |  | [optional] |

### Return type

[**Array&lt;Coupon&gt;**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_coupon

> <Coupon> update_coupon(coupon_id, coupon_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CouponApi.new
coupon_id = 'coupon_id_example' # String | 
coupon_update = SimplebillyApi::CouponUpdate.new # CouponUpdate | 

begin
  
  result = api_instance.update_coupon(coupon_id, coupon_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->update_coupon: #{e}"
end
```

#### Using the update_coupon_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Coupon>, Integer, Hash)> update_coupon_with_http_info(coupon_id, coupon_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_coupon_with_http_info(coupon_id, coupon_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Coupon>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CouponApi->update_coupon_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **coupon_id** | **String** |  |  |
| **coupon_update** | [**CouponUpdate**](CouponUpdate.md) |  |  |

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

