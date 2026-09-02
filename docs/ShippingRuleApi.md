# SimplebillyApi::ShippingRuleApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_shipping_rule**](ShippingRuleApi.md#create_shipping_rule) | **POST** /api/v1/shipping-rules |  |
| [**delete_shipping_rule**](ShippingRuleApi.md#delete_shipping_rule) | **DELETE** /api/v1/shipping-rules/{rule_id} |  |
| [**get_shipping_rule**](ShippingRuleApi.md#get_shipping_rule) | **GET** /api/v1/shipping-rules/{rule_id} |  |
| [**list_shipping_rules**](ShippingRuleApi.md#list_shipping_rules) | **GET** /api/v1/shipping-rules/ |  |
| [**update_shipping_rule**](ShippingRuleApi.md#update_shipping_rule) | **PUT** /api/v1/shipping-rules/{rule_id} |  |


## create_shipping_rule

> <ShippingRule> create_shipping_rule(shipping_rule_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingRuleApi.new
shipping_rule_create = SimplebillyApi::ShippingRuleCreate.new({name: 'name_example', price: 'price_example'}) # ShippingRuleCreate | 

begin
  
  result = api_instance.create_shipping_rule(shipping_rule_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->create_shipping_rule: #{e}"
end
```

#### Using the create_shipping_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingRule>, Integer, Hash)> create_shipping_rule_with_http_info(shipping_rule_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_shipping_rule_with_http_info(shipping_rule_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingRule>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->create_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipping_rule_create** | [**ShippingRuleCreate**](ShippingRuleCreate.md) |  |  |

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_shipping_rule

> delete_shipping_rule(rule_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingRuleApi.new
rule_id = 'rule_id_example' # String | 

begin
  
  api_instance.delete_shipping_rule(rule_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->delete_shipping_rule: #{e}"
end
```

#### Using the delete_shipping_rule_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_shipping_rule_with_http_info(rule_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_shipping_rule_with_http_info(rule_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->delete_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_shipping_rule

> <ShippingRule> get_shipping_rule(rule_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingRuleApi.new
rule_id = 'rule_id_example' # String | 

begin
  
  result = api_instance.get_shipping_rule(rule_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->get_shipping_rule: #{e}"
end
```

#### Using the get_shipping_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingRule>, Integer, Hash)> get_shipping_rule_with_http_info(rule_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_shipping_rule_with_http_info(rule_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingRule>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->get_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** |  |  |

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_shipping_rules

> <Array<ShippingRule>> list_shipping_rules(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingRuleApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  country: 'country_example' # String | 
}

begin
  
  result = api_instance.list_shipping_rules(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->list_shipping_rules: #{e}"
end
```

#### Using the list_shipping_rules_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ShippingRule>>, Integer, Hash)> list_shipping_rules_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_shipping_rules_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ShippingRule>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->list_shipping_rules_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **country** | **String** |  | [optional] |

### Return type

[**Array&lt;ShippingRule&gt;**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_shipping_rule

> <ShippingRule> update_shipping_rule(rule_id, shipping_rule_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShippingRuleApi.new
rule_id = 'rule_id_example' # String | 
shipping_rule_update = SimplebillyApi::ShippingRuleUpdate.new # ShippingRuleUpdate | 

begin
  
  result = api_instance.update_shipping_rule(rule_id, shipping_rule_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->update_shipping_rule: #{e}"
end
```

#### Using the update_shipping_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ShippingRule>, Integer, Hash)> update_shipping_rule_with_http_info(rule_id, shipping_rule_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_shipping_rule_with_http_info(rule_id, shipping_rule_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ShippingRule>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShippingRuleApi->update_shipping_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** |  |  |
| **shipping_rule_update** | [**ShippingRuleUpdate**](ShippingRuleUpdate.md) |  |  |

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

