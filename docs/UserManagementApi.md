# SimplebillyApi::UserManagementApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_user**](UserManagementApi.md#get_user) | **GET** /api/v1/users/{user_id} |  |
| [**list_users**](UserManagementApi.md#list_users) | **GET** /api/v1/users |  |
| [**remove_user**](UserManagementApi.md#remove_user) | **DELETE** /api/v1/users/{user_id} |  |
| [**update_user_permissions**](UserManagementApi.md#update_user_permissions) | **PUT** /api/v1/users/{user_id}/permissions |  |
| [**update_user_role**](UserManagementApi.md#update_user_role) | **PUT** /api/v1/users/{user_id}/role |  |


## get_user

> <TenantUser> get_user(user_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserManagementApi.new
user_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_user(user_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->get_user: #{e}"
end
```

#### Using the get_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TenantUser>, Integer, Hash)> get_user_with_http_info(user_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_user_with_http_info(user_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TenantUser>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->get_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |

### Return type

[**TenantUser**](TenantUser.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_users

> <Array<TenantUser>> list_users



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserManagementApi.new

begin
  
  result = api_instance.list_users
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->list_users: #{e}"
end
```

#### Using the list_users_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<TenantUser>>, Integer, Hash)> list_users_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_users_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<TenantUser>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->list_users_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;TenantUser&gt;**](TenantUser.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## remove_user

> remove_user(user_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserManagementApi.new
user_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.remove_user(user_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->remove_user: #{e}"
end
```

#### Using the remove_user_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> remove_user_with_http_info(user_id)

```ruby
begin
  
  data, status_code, headers = api_instance.remove_user_with_http_info(user_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->remove_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## update_user_permissions

> update_user_permissions(user_id, update_permissions_payload)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserManagementApi.new
user_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
update_permissions_payload = SimplebillyApi::UpdatePermissionsPayload.new({permissions: ['permissions_example']}) # UpdatePermissionsPayload | 

begin
  
  api_instance.update_user_permissions(user_id, update_permissions_payload)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->update_user_permissions: #{e}"
end
```

#### Using the update_user_permissions_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_user_permissions_with_http_info(user_id, update_permissions_payload)

```ruby
begin
  
  data, status_code, headers = api_instance.update_user_permissions_with_http_info(user_id, update_permissions_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->update_user_permissions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **update_permissions_payload** | [**UpdatePermissionsPayload**](UpdatePermissionsPayload.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## update_user_role

> update_user_role(user_id, update_role_payload)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserManagementApi.new
user_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
update_role_payload = SimplebillyApi::UpdateRolePayload.new({role: 'role_example'}) # UpdateRolePayload | 

begin
  
  api_instance.update_user_role(user_id, update_role_payload)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->update_user_role: #{e}"
end
```

#### Using the update_user_role_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_user_role_with_http_info(user_id, update_role_payload)

```ruby
begin
  
  data, status_code, headers = api_instance.update_user_role_with_http_info(user_id, update_role_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserManagementApi->update_user_role_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **String** |  |  |
| **update_role_payload** | [**UpdateRolePayload**](UpdateRolePayload.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

