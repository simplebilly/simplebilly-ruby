# SimplebillyApi::AdminApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**trigger_mirror**](AdminApi.md#trigger_mirror) | **POST** /api/v1/admin/storage/mirror |  |


## trigger_mirror

> <MirrorTriggerResponse> trigger_mirror



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AdminApi.new

begin
  
  result = api_instance.trigger_mirror
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AdminApi->trigger_mirror: #{e}"
end
```

#### Using the trigger_mirror_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MirrorTriggerResponse>, Integer, Hash)> trigger_mirror_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.trigger_mirror_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MirrorTriggerResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AdminApi->trigger_mirror_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**MirrorTriggerResponse**](MirrorTriggerResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

