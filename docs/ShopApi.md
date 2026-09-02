# SimplebillyApi::ShopApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**shop_editor_save**](ShopApi.md#shop_editor_save) | **POST** /api/v1/shop/editor |  |


## shop_editor_save

> Object shop_editor_save(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ShopApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.shop_editor_save(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShopApi->shop_editor_save: #{e}"
end
```

#### Using the shop_editor_save_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> shop_editor_save_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.shop_editor_save_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ShopApi->shop_editor_save_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

