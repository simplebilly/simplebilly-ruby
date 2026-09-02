# SimplebillyApi::PaymentConditionApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_payment_conditions_api**](PaymentConditionApi.md#list_payment_conditions_api) | **GET** /api/v1/payment-conditions |  |


## list_payment_conditions_api

> <Array<PaymentCondition>> list_payment_conditions_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PaymentConditionApi.new

begin
  
  result = api_instance.list_payment_conditions_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentConditionApi->list_payment_conditions_api: #{e}"
end
```

#### Using the list_payment_conditions_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PaymentCondition>>, Integer, Hash)> list_payment_conditions_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_payment_conditions_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PaymentCondition>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PaymentConditionApi->list_payment_conditions_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;PaymentCondition&gt;**](PaymentCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

