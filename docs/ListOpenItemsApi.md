# SimplebillyApi::ListOpenItemsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_open_items_api**](ListOpenItemsApi.md#list_open_items_api) | **GET** /api/v1/bookkeeping/open-items |  |


## list_open_items_api

> <Array<OpenItem>> list_open_items_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ListOpenItemsApi.new
opts = {
  reminder_level1_days: 789, # Integer | 
  reminder_level2_days: 789, # Integer | 
  reminder_level3_days: 789, # Integer | 
  customer_id: 'customer_id_example' # String | 
}

begin
  
  result = api_instance.list_open_items_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ListOpenItemsApi->list_open_items_api: #{e}"
end
```

#### Using the list_open_items_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<OpenItem>>, Integer, Hash)> list_open_items_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_open_items_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<OpenItem>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ListOpenItemsApi->list_open_items_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reminder_level1_days** | **Integer** |  | [optional] |
| **reminder_level2_days** | **Integer** |  | [optional] |
| **reminder_level3_days** | **Integer** |  | [optional] |
| **customer_id** | **String** |  | [optional] |

### Return type

[**Array&lt;OpenItem&gt;**](OpenItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

