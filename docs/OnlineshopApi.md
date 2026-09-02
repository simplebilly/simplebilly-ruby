# SimplebillyApi::OnlineshopApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_smtp_config_api**](OnlineshopApi.md#get_smtp_config_api) | **GET** /api/v1/settings/smtp |  |
| [**save_smtp_config_api**](OnlineshopApi.md#save_smtp_config_api) | **PUT** /api/v1/settings/smtp |  |


## get_smtp_config_api

> <SmtpConfig> get_smtp_config_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OnlineshopApi.new

begin
  
  result = api_instance.get_smtp_config_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OnlineshopApi->get_smtp_config_api: #{e}"
end
```

#### Using the get_smtp_config_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SmtpConfig>, Integer, Hash)> get_smtp_config_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.get_smtp_config_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SmtpConfig>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OnlineshopApi->get_smtp_config_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**SmtpConfig**](SmtpConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## save_smtp_config_api

> <SmtpConfig> save_smtp_config_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::OnlineshopApi.new
opts = {
  smtp_config: SimplebillyApi::SmtpConfig.new({encryption: SimplebillyApi::SmtpEncryption::START_TLS, from_address: 'from_address_example', host: 'host_example', password: 'password_example', port: 37, username: 'username_example'}) # SmtpConfig | 
}

begin
  
  result = api_instance.save_smtp_config_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OnlineshopApi->save_smtp_config_api: #{e}"
end
```

#### Using the save_smtp_config_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SmtpConfig>, Integer, Hash)> save_smtp_config_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.save_smtp_config_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SmtpConfig>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling OnlineshopApi->save_smtp_config_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **smtp_config** | [**SmtpConfig**](SmtpConfig.md) |  | [optional] |

### Return type

[**SmtpConfig**](SmtpConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

