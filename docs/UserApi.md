# SimplebillyApi::UserApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**change_password**](UserApi.md#change_password) | **POST** /user/change-password | Change the current user&#39;s password (requires the current password). |
| [**create_team**](UserApi.md#create_team) | **POST** /user/teams | Create a new team within the current tenant |
| [**generate_api_key**](UserApi.md#generate_api_key) | **POST** /user/api-key | Generate a new API key for the current user |
| [**invite_user**](UserApi.md#invite_user) | **POST** /user/invite | Invite a user to the current tenant/organization |
| [**list_teams**](UserApi.md#list_teams) | **GET** /user/teams | List all teams in the current tenant |
| [**remove_user_from_org**](UserApi.md#remove_user_from_org) | **DELETE** /user/remove | Remove a user from the current organization |
| [**update_profile**](UserApi.md#update_profile) | **PUT** /user/profile | Update the current user&#39;s profile |
| [**user_profile**](UserApi.md#user_profile) | **GET** /user/profile | Get the current user&#39;s profile |
| [**user_tenants**](UserApi.md#user_tenants) | **GET** /user/tenants | List all tenants (organizations) the current user belongs to |


## change_password

> change_password(change_password_request)

Change the current user's password (requires the current password).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new
change_password_request = SimplebillyApi::ChangePasswordRequest.new({current_password: 'current_password_example', new_password: 'new_password_example'}) # ChangePasswordRequest | 

begin
  # Change the current user's password (requires the current password).
  api_instance.change_password(change_password_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->change_password: #{e}"
end
```

#### Using the change_password_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> change_password_with_http_info(change_password_request)

```ruby
begin
  # Change the current user's password (requires the current password).
  data, status_code, headers = api_instance.change_password_with_http_info(change_password_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->change_password_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **change_password_request** | [**ChangePasswordRequest**](ChangePasswordRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## create_team

> <ApiResponseTeam> create_team(team_create)

Create a new team within the current tenant

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new
team_create = SimplebillyApi::TeamCreate.new({name: 'name_example'}) # TeamCreate | 

begin
  # Create a new team within the current tenant
  result = api_instance.create_team(team_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->create_team: #{e}"
end
```

#### Using the create_team_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseTeam>, Integer, Hash)> create_team_with_http_info(team_create)

```ruby
begin
  # Create a new team within the current tenant
  data, status_code, headers = api_instance.create_team_with_http_info(team_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseTeam>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->create_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **team_create** | [**TeamCreate**](TeamCreate.md) |  |  |

### Return type

[**ApiResponseTeam**](ApiResponseTeam.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_api_key

> <ApiResponseString> generate_api_key

Generate a new API key for the current user

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new

begin
  # Generate a new API key for the current user
  result = api_instance.generate_api_key
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->generate_api_key: #{e}"
end
```

#### Using the generate_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseString>, Integer, Hash)> generate_api_key_with_http_info

```ruby
begin
  # Generate a new API key for the current user
  data, status_code, headers = api_instance.generate_api_key_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseString>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->generate_api_key_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiResponseString**](ApiResponseString.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## invite_user

> invite_user(invite_request)

Invite a user to the current tenant/organization

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new
invite_request = SimplebillyApi::InviteRequest.new({email: 'email_example'}) # InviteRequest | 

begin
  # Invite a user to the current tenant/organization
  api_instance.invite_user(invite_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->invite_user: #{e}"
end
```

#### Using the invite_user_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> invite_user_with_http_info(invite_request)

```ruby
begin
  # Invite a user to the current tenant/organization
  data, status_code, headers = api_instance.invite_user_with_http_info(invite_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->invite_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invite_request** | [**InviteRequest**](InviteRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## list_teams

> <ApiResponseVecTeam> list_teams

List all teams in the current tenant

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new

begin
  # List all teams in the current tenant
  result = api_instance.list_teams
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->list_teams: #{e}"
end
```

#### Using the list_teams_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseVecTeam>, Integer, Hash)> list_teams_with_http_info

```ruby
begin
  # List all teams in the current tenant
  data, status_code, headers = api_instance.list_teams_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseVecTeam>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->list_teams_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiResponseVecTeam**](ApiResponseVecTeam.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## remove_user_from_org

> remove_user_from_org(remove_user_request)

Remove a user from the current organization

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new
remove_user_request = SimplebillyApi::RemoveUserRequest.new({email: 'email_example'}) # RemoveUserRequest | 

begin
  # Remove a user from the current organization
  api_instance.remove_user_from_org(remove_user_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->remove_user_from_org: #{e}"
end
```

#### Using the remove_user_from_org_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> remove_user_from_org_with_http_info(remove_user_request)

```ruby
begin
  # Remove a user from the current organization
  data, status_code, headers = api_instance.remove_user_from_org_with_http_info(remove_user_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->remove_user_from_org_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **remove_user_request** | [**RemoveUserRequest**](RemoveUserRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## update_profile

> update_profile(update_profile_request)

Update the current user's profile

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new
update_profile_request = SimplebillyApi::UpdateProfileRequest.new # UpdateProfileRequest | 

begin
  # Update the current user's profile
  api_instance.update_profile(update_profile_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->update_profile: #{e}"
end
```

#### Using the update_profile_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_profile_with_http_info(update_profile_request)

```ruby
begin
  # Update the current user's profile
  data, status_code, headers = api_instance.update_profile_with_http_info(update_profile_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->update_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **update_profile_request** | [**UpdateProfileRequest**](UpdateProfileRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## user_profile

> <ApiResponseUserProfile> user_profile

Get the current user's profile

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new

begin
  # Get the current user's profile
  result = api_instance.user_profile
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->user_profile: #{e}"
end
```

#### Using the user_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseUserProfile>, Integer, Hash)> user_profile_with_http_info

```ruby
begin
  # Get the current user's profile
  data, status_code, headers = api_instance.user_profile_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseUserProfile>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->user_profile_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiResponseUserProfile**](ApiResponseUserProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## user_tenants

> <ApiResponseVecUserTenantInfo> user_tenants

List all tenants (organizations) the current user belongs to

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::UserApi.new

begin
  # List all tenants (organizations) the current user belongs to
  result = api_instance.user_tenants
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->user_tenants: #{e}"
end
```

#### Using the user_tenants_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseVecUserTenantInfo>, Integer, Hash)> user_tenants_with_http_info

```ruby
begin
  # List all tenants (organizations) the current user belongs to
  data, status_code, headers = api_instance.user_tenants_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseVecUserTenantInfo>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling UserApi->user_tenants_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiResponseVecUserTenantInfo**](ApiResponseVecUserTenantInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

