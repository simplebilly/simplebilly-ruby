# SimplebillyApi::PriceTierApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_price_tier**](PriceTierApi.md#create_price_tier) | **POST** /api/v1/price-tiers |  |
| [**delete_price_tier**](PriceTierApi.md#delete_price_tier) | **DELETE** /api/v1/price-tiers/{price_tier_id} |  |
| [**get_price_tier**](PriceTierApi.md#get_price_tier) | **GET** /api/v1/price-tiers/{price_tier_id} |  |
| [**get_resolved_price**](PriceTierApi.md#get_resolved_price) | **GET** /api/v1/price-tiers/resolved |  |
| [**list_price_tiers**](PriceTierApi.md#list_price_tiers) | **GET** /api/v1/price-tiers/ |  |
| [**update_price_tier**](PriceTierApi.md#update_price_tier) | **PUT** /api/v1/price-tiers/{price_tier_id} |  |


## create_price_tier

> <PriceTier> create_price_tier(price_tier_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PriceTierApi.new
price_tier_create = SimplebillyApi::PriceTierCreate.new({product_id: 'product_id_example', unit_price: 'unit_price_example'}) # PriceTierCreate | 

begin
  
  result = api_instance.create_price_tier(price_tier_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->create_price_tier: #{e}"
end
```

#### Using the create_price_tier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PriceTier>, Integer, Hash)> create_price_tier_with_http_info(price_tier_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_price_tier_with_http_info(price_tier_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PriceTier>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->create_price_tier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price_tier_create** | [**PriceTierCreate**](PriceTierCreate.md) |  |  |

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_price_tier

> delete_price_tier(price_tier_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PriceTierApi.new
price_tier_id = 'price_tier_id_example' # String | 

begin
  
  api_instance.delete_price_tier(price_tier_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->delete_price_tier: #{e}"
end
```

#### Using the delete_price_tier_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_price_tier_with_http_info(price_tier_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_price_tier_with_http_info(price_tier_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->delete_price_tier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price_tier_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_price_tier

> <PriceTier> get_price_tier(price_tier_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PriceTierApi.new
price_tier_id = 'price_tier_id_example' # String | 

begin
  
  result = api_instance.get_price_tier(price_tier_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->get_price_tier: #{e}"
end
```

#### Using the get_price_tier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PriceTier>, Integer, Hash)> get_price_tier_with_http_info(price_tier_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_price_tier_with_http_info(price_tier_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PriceTier>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->get_price_tier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price_tier_id** | **String** |  |  |

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_resolved_price

> <ResolvedPriceResponse> get_resolved_price(product_id, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PriceTierApi.new
product_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
opts = {
  quantity: 789, # Integer | 
  contact_id: 'contact_id_example' # String | Contact used to match customer-group-scoped tiers.
}

begin
  
  result = api_instance.get_resolved_price(product_id, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->get_resolved_price: #{e}"
end
```

#### Using the get_resolved_price_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ResolvedPriceResponse>, Integer, Hash)> get_resolved_price_with_http_info(product_id, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_resolved_price_with_http_info(product_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ResolvedPriceResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->get_resolved_price_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** |  |  |
| **quantity** | **Integer** |  | [optional] |
| **contact_id** | **String** | Contact used to match customer-group-scoped tiers. | [optional] |

### Return type

[**ResolvedPriceResponse**](ResolvedPriceResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_price_tiers

> <Array<PriceTier>> list_price_tiers(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PriceTierApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  product_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  customer_group_id: 'customer_group_id_example' # String | 
}

begin
  
  result = api_instance.list_price_tiers(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->list_price_tiers: #{e}"
end
```

#### Using the list_price_tiers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PriceTier>>, Integer, Hash)> list_price_tiers_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_price_tiers_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PriceTier>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->list_price_tiers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **product_id** | **String** |  | [optional] |
| **customer_group_id** | **String** |  | [optional] |

### Return type

[**Array&lt;PriceTier&gt;**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_price_tier

> <PriceTier> update_price_tier(price_tier_id, price_tier_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PriceTierApi.new
price_tier_id = 'price_tier_id_example' # String | 
price_tier_update = SimplebillyApi::PriceTierUpdate.new({unit_price: 'unit_price_example'}) # PriceTierUpdate | 

begin
  
  result = api_instance.update_price_tier(price_tier_id, price_tier_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->update_price_tier: #{e}"
end
```

#### Using the update_price_tier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PriceTier>, Integer, Hash)> update_price_tier_with_http_info(price_tier_id, price_tier_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_price_tier_with_http_info(price_tier_id, price_tier_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PriceTier>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PriceTierApi->update_price_tier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price_tier_id** | **String** |  |  |
| **price_tier_update** | [**PriceTierUpdate**](PriceTierUpdate.md) |  |  |

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

