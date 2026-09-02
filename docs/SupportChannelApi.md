# SimplebillyApi::SupportChannelApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_channel_api**](SupportChannelApi.md#create_channel_api) | **POST** /api/v1/support/channels |  |
| [**delete_channel_api**](SupportChannelApi.md#delete_channel_api) | **DELETE** /api/v1/support/channels/{channel_id} |  |
| [**list_channels_api**](SupportChannelApi.md#list_channels_api) | **GET** /api/v1/support/channels |  |
| [**update_channel_api**](SupportChannelApi.md#update_channel_api) | **PUT** /api/v1/support/channels/{channel_id} |  |


## create_channel_api

> <SupportChannel> create_channel_api(create_channel_dto)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportChannelApi.new
create_channel_dto = SimplebillyApi::CreateChannelDto.new({channel_type: 'channel_type_example', config: 3.56, name: 'name_example'}) # CreateChannelDto | 

begin
  
  result = api_instance.create_channel_api(create_channel_dto)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->create_channel_api: #{e}"
end
```

#### Using the create_channel_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupportChannel>, Integer, Hash)> create_channel_api_with_http_info(create_channel_dto)

```ruby
begin
  
  data, status_code, headers = api_instance.create_channel_api_with_http_info(create_channel_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupportChannel>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->create_channel_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_channel_dto** | [**CreateChannelDto**](CreateChannelDto.md) |  |  |

### Return type

[**SupportChannel**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_channel_api

> delete_channel_api(channel_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportChannelApi.new
channel_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_channel_api(channel_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->delete_channel_api: #{e}"
end
```

#### Using the delete_channel_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_channel_api_with_http_info(channel_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_channel_api_with_http_info(channel_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->delete_channel_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_channels_api

> <Array<SupportChannel>> list_channels_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportChannelApi.new

begin
  
  result = api_instance.list_channels_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->list_channels_api: #{e}"
end
```

#### Using the list_channels_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<SupportChannel>>, Integer, Hash)> list_channels_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_channels_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<SupportChannel>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->list_channels_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;SupportChannel&gt;**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_channel_api

> <SupportChannel> update_channel_api(channel_id, update_channel_dto)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::SupportChannelApi.new
channel_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
update_channel_dto = SimplebillyApi::UpdateChannelDto.new # UpdateChannelDto | 

begin
  
  result = api_instance.update_channel_api(channel_id, update_channel_dto)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->update_channel_api: #{e}"
end
```

#### Using the update_channel_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SupportChannel>, Integer, Hash)> update_channel_api_with_http_info(channel_id, update_channel_dto)

```ruby
begin
  
  data, status_code, headers = api_instance.update_channel_api_with_http_info(channel_id, update_channel_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SupportChannel>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling SupportChannelApi->update_channel_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_id** | **String** |  |  |
| **update_channel_dto** | [**UpdateChannelDto**](UpdateChannelDto.md) |  |  |

### Return type

[**SupportChannel**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

