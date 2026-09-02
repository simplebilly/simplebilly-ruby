# SimplebillyApi::MarketplaceApiApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_connection_api**](MarketplaceApiApi.md#create_connection_api) | **POST** /api/v1/marketplace/connections | Create a new connection (for API-key based platforms) |
| [**delete_connection_api**](MarketplaceApiApi.md#delete_connection_api) | **DELETE** /api/v1/marketplace/connections/{connection_id} | Soft-delete a connection |
| [**get_connection_api**](MarketplaceApiApi.md#get_connection_api) | **GET** /api/v1/marketplace/connections/{connection_id} | Get a single connection |
| [**get_sync_direction_api**](MarketplaceApiApi.md#get_sync_direction_api) | **GET** /api/v1/marketplace/connections/{connection_id}/directions | Get current sync direction configuration for a connection |
| [**get_sync_logs_api**](MarketplaceApiApi.md#get_sync_logs_api) | **GET** /api/v1/marketplace/connections/{connection_id}/logs | Get sync logs for a connection |
| [**list_connections_api**](MarketplaceApiApi.md#list_connections_api) | **GET** /api/v1/marketplace/connections | List connections for the current tenant |
| [**list_platforms_api**](MarketplaceApiApi.md#list_platforms_api) | **GET** /api/v1/marketplace/platforms | List all supported platforms |
| [**oauth_authorize_api**](MarketplaceApiApi.md#oauth_authorize_api) | **POST** /api/v1/marketplace/oauth/authorize | OAuth: initiate authorization flow |
| [**oauth_callback_api**](MarketplaceApiApi.md#oauth_callback_api) | **POST** /api/v1/marketplace/oauth/callback | OAuth: handle callback after authorization |
| [**trigger_sync_api**](MarketplaceApiApi.md#trigger_sync_api) | **POST** /api/v1/marketplace/connections/{connection_id}/sync | Trigger sync for a connection |
| [**update_connection_api**](MarketplaceApiApi.md#update_connection_api) | **PUT** /api/v1/marketplace/connections/{connection_id} | Update a connection |
| [**update_sync_direction_api**](MarketplaceApiApi.md#update_sync_direction_api) | **PUT** /api/v1/marketplace/connections/{connection_id}/directions | Update per-entity sync direction configuration for a connection |
| [**webhook_receiver_api**](MarketplaceApiApi.md#webhook_receiver_api) | **POST** /api/v1/marketplace/webhook/{platform}/{connection_id} | Webhook receiver |


## create_connection_api

> <MarketplaceConnection> create_connection_api(create_connection_request)

Create a new connection (for API-key based platforms)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
create_connection_request = SimplebillyApi::CreateConnectionRequest.new({label: 'label_example', platform: 'platform_example'}) # CreateConnectionRequest | 

begin
  # Create a new connection (for API-key based platforms)
  result = api_instance.create_connection_api(create_connection_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->create_connection_api: #{e}"
end
```

#### Using the create_connection_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MarketplaceConnection>, Integer, Hash)> create_connection_api_with_http_info(create_connection_request)

```ruby
begin
  # Create a new connection (for API-key based platforms)
  data, status_code, headers = api_instance.create_connection_api_with_http_info(create_connection_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MarketplaceConnection>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->create_connection_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_connection_request** | [**CreateConnectionRequest**](CreateConnectionRequest.md) |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_connection_api

> delete_connection_api(connection_id)

Soft-delete a connection

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
connection_id = 'connection_id_example' # String | 

begin
  # Soft-delete a connection
  api_instance.delete_connection_api(connection_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->delete_connection_api: #{e}"
end
```

#### Using the delete_connection_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_connection_api_with_http_info(connection_id)

```ruby
begin
  # Soft-delete a connection
  data, status_code, headers = api_instance.delete_connection_api_with_http_info(connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->delete_connection_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_connection_api

> <MarketplaceConnection> get_connection_api(connection_id)

Get a single connection

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
connection_id = 'connection_id_example' # String | 

begin
  # Get a single connection
  result = api_instance.get_connection_api(connection_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->get_connection_api: #{e}"
end
```

#### Using the get_connection_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MarketplaceConnection>, Integer, Hash)> get_connection_api_with_http_info(connection_id)

```ruby
begin
  # Get a single connection
  data, status_code, headers = api_instance.get_connection_api_with_http_info(connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MarketplaceConnection>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->get_connection_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_sync_direction_api

> get_sync_direction_api(connection_id)

Get current sync direction configuration for a connection

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
connection_id = 'connection_id_example' # String | 

begin
  # Get current sync direction configuration for a connection
  api_instance.get_sync_direction_api(connection_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->get_sync_direction_api: #{e}"
end
```

#### Using the get_sync_direction_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> get_sync_direction_api_with_http_info(connection_id)

```ruby
begin
  # Get current sync direction configuration for a connection
  data, status_code, headers = api_instance.get_sync_direction_api_with_http_info(connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->get_sync_direction_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_sync_logs_api

> <Array<SyncLog>> get_sync_logs_api(connection_id)

Get sync logs for a connection

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
connection_id = 'connection_id_example' # String | 

begin
  # Get sync logs for a connection
  result = api_instance.get_sync_logs_api(connection_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->get_sync_logs_api: #{e}"
end
```

#### Using the get_sync_logs_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<SyncLog>>, Integer, Hash)> get_sync_logs_api_with_http_info(connection_id)

```ruby
begin
  # Get sync logs for a connection
  data, status_code, headers = api_instance.get_sync_logs_api_with_http_info(connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<SyncLog>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->get_sync_logs_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |

### Return type

[**Array&lt;SyncLog&gt;**](SyncLog.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_connections_api

> <Array<MarketplaceConnection>> list_connections_api

List connections for the current tenant

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new

begin
  # List connections for the current tenant
  result = api_instance.list_connections_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->list_connections_api: #{e}"
end
```

#### Using the list_connections_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<MarketplaceConnection>>, Integer, Hash)> list_connections_api_with_http_info

```ruby
begin
  # List connections for the current tenant
  data, status_code, headers = api_instance.list_connections_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<MarketplaceConnection>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->list_connections_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;MarketplaceConnection&gt;**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_platforms_api

> <Array<PlatformInfo>> list_platforms_api

List all supported platforms

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new

begin
  # List all supported platforms
  result = api_instance.list_platforms_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->list_platforms_api: #{e}"
end
```

#### Using the list_platforms_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PlatformInfo>>, Integer, Hash)> list_platforms_api_with_http_info

```ruby
begin
  # List all supported platforms
  data, status_code, headers = api_instance.list_platforms_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PlatformInfo>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->list_platforms_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;PlatformInfo&gt;**](PlatformInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## oauth_authorize_api

> <OAuthAuthorizeResponse> oauth_authorize_api(o_auth_authorize_request)

OAuth: initiate authorization flow

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
o_auth_authorize_request = SimplebillyApi::OAuthAuthorizeRequest.new({platform: 'platform_example', redirect_uri: 'redirect_uri_example'}) # OAuthAuthorizeRequest | 

begin
  # OAuth: initiate authorization flow
  result = api_instance.oauth_authorize_api(o_auth_authorize_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->oauth_authorize_api: #{e}"
end
```

#### Using the oauth_authorize_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OAuthAuthorizeResponse>, Integer, Hash)> oauth_authorize_api_with_http_info(o_auth_authorize_request)

```ruby
begin
  # OAuth: initiate authorization flow
  data, status_code, headers = api_instance.oauth_authorize_api_with_http_info(o_auth_authorize_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OAuthAuthorizeResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->oauth_authorize_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **o_auth_authorize_request** | [**OAuthAuthorizeRequest**](OAuthAuthorizeRequest.md) |  |  |

### Return type

[**OAuthAuthorizeResponse**](OAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## oauth_callback_api

> <MarketplaceConnection> oauth_callback_api(o_auth_callback_request)

OAuth: handle callback after authorization

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
o_auth_callback_request = SimplebillyApi::OAuthCallbackRequest.new({code: 'code_example', platform: 'platform_example', state: 'state_example'}) # OAuthCallbackRequest | 

begin
  # OAuth: handle callback after authorization
  result = api_instance.oauth_callback_api(o_auth_callback_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->oauth_callback_api: #{e}"
end
```

#### Using the oauth_callback_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MarketplaceConnection>, Integer, Hash)> oauth_callback_api_with_http_info(o_auth_callback_request)

```ruby
begin
  # OAuth: handle callback after authorization
  data, status_code, headers = api_instance.oauth_callback_api_with_http_info(o_auth_callback_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MarketplaceConnection>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->oauth_callback_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **o_auth_callback_request** | [**OAuthCallbackRequest**](OAuthCallbackRequest.md) |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## trigger_sync_api

> <SyncSummary> trigger_sync_api(connection_id, opts)

Trigger sync for a connection

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
connection_id = 'connection_id_example' # String | 
opts = {
  sync_type: 'sync_type_example', # String | 
  direction: 'direction_example' # String | 
}

begin
  # Trigger sync for a connection
  result = api_instance.trigger_sync_api(connection_id, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->trigger_sync_api: #{e}"
end
```

#### Using the trigger_sync_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SyncSummary>, Integer, Hash)> trigger_sync_api_with_http_info(connection_id, opts)

```ruby
begin
  # Trigger sync for a connection
  data, status_code, headers = api_instance.trigger_sync_api_with_http_info(connection_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SyncSummary>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->trigger_sync_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **sync_type** | **String** |  | [optional] |
| **direction** | **String** |  | [optional] |

### Return type

[**SyncSummary**](SyncSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_connection_api

> <MarketplaceConnection> update_connection_api(connection_id, update_connection_request)

Update a connection

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
connection_id = 'connection_id_example' # String | 
update_connection_request = SimplebillyApi::UpdateConnectionRequest.new # UpdateConnectionRequest | 

begin
  # Update a connection
  result = api_instance.update_connection_api(connection_id, update_connection_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->update_connection_api: #{e}"
end
```

#### Using the update_connection_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MarketplaceConnection>, Integer, Hash)> update_connection_api_with_http_info(connection_id, update_connection_request)

```ruby
begin
  # Update a connection
  data, status_code, headers = api_instance.update_connection_api_with_http_info(connection_id, update_connection_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MarketplaceConnection>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->update_connection_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **update_connection_request** | [**UpdateConnectionRequest**](UpdateConnectionRequest.md) |  |  |

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_sync_direction_api

> update_sync_direction_api(connection_id, update_sync_direction_request)

Update per-entity sync direction configuration for a connection

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
connection_id = 'connection_id_example' # String | 
update_sync_direction_request = SimplebillyApi::UpdateSyncDirectionRequest.new({directions: { key: 'inner_example'}}) # UpdateSyncDirectionRequest | 

begin
  # Update per-entity sync direction configuration for a connection
  api_instance.update_sync_direction_api(connection_id, update_sync_direction_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->update_sync_direction_api: #{e}"
end
```

#### Using the update_sync_direction_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_sync_direction_api_with_http_info(connection_id, update_sync_direction_request)

```ruby
begin
  # Update per-entity sync direction configuration for a connection
  data, status_code, headers = api_instance.update_sync_direction_api_with_http_info(connection_id, update_sync_direction_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->update_sync_direction_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **update_sync_direction_request** | [**UpdateSyncDirectionRequest**](UpdateSyncDirectionRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## webhook_receiver_api

> webhook_receiver_api(platform, connection_id)

Webhook receiver

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::MarketplaceApiApi.new
platform = 'platform_example' # String | 
connection_id = 'connection_id_example' # String | 

begin
  # Webhook receiver
  api_instance.webhook_receiver_api(platform, connection_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->webhook_receiver_api: #{e}"
end
```

#### Using the webhook_receiver_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> webhook_receiver_api_with_http_info(platform, connection_id)

```ruby
begin
  # Webhook receiver
  data, status_code, headers = api_instance.webhook_receiver_api_with_http_info(platform, connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling MarketplaceApiApi->webhook_receiver_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  |  |
| **connection_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

