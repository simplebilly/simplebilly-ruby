# SimplebillyApi::TenantSettingsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_tenant_settings**](TenantSettingsApi.md#get_tenant_settings) | **GET** /api/v1/settings/tenant |  |
| [**update_tenant_settings**](TenantSettingsApi.md#update_tenant_settings) | **PUT** /api/v1/settings/tenant |  |


## get_tenant_settings

> <TenantSettings> get_tenant_settings



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TenantSettingsApi.new

begin
  
  result = api_instance.get_tenant_settings
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TenantSettingsApi->get_tenant_settings: #{e}"
end
```

#### Using the get_tenant_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TenantSettings>, Integer, Hash)> get_tenant_settings_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.get_tenant_settings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TenantSettings>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TenantSettingsApi->get_tenant_settings_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_tenant_settings

> <TenantSettings> update_tenant_settings(update_tenant_settings)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TenantSettingsApi.new
update_tenant_settings = SimplebillyApi::UpdateTenantSettings.new({company_type: SimplebillyApi::CompanyType::GMBH}) # UpdateTenantSettings | 

begin
  
  result = api_instance.update_tenant_settings(update_tenant_settings)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TenantSettingsApi->update_tenant_settings: #{e}"
end
```

#### Using the update_tenant_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TenantSettings>, Integer, Hash)> update_tenant_settings_with_http_info(update_tenant_settings)

```ruby
begin
  
  data, status_code, headers = api_instance.update_tenant_settings_with_http_info(update_tenant_settings)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TenantSettings>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TenantSettingsApi->update_tenant_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **update_tenant_settings** | [**UpdateTenantSettings**](UpdateTenantSettings.md) |  |  |

### Return type

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

