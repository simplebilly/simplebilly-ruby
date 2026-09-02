# SimplebillyApi::EmissionsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_emission_entry_api**](EmissionsApi.md#create_emission_entry_api) | **POST** /api/v1/bookkeeping/emissions/entries |  |
| [**create_emission_target_api**](EmissionsApi.md#create_emission_target_api) | **POST** /api/v1/bookkeeping/emissions/targets |  |
| [**delete_emission_entry_api**](EmissionsApi.md#delete_emission_entry_api) | **DELETE** /api/v1/bookkeeping/emissions/entries/{id} |  |
| [**delete_emission_target_api**](EmissionsApi.md#delete_emission_target_api) | **DELETE** /api/v1/bookkeeping/emissions/targets/{id} |  |
| [**emissions_entries_api**](EmissionsApi.md#emissions_entries_api) | **GET** /api/v1/bookkeeping/emissions/entries |  |
| [**emissions_export_api**](EmissionsApi.md#emissions_export_api) | **GET** /api/v1/bookkeeping/emissions/export |  |
| [**emissions_factors_api**](EmissionsApi.md#emissions_factors_api) | **GET** /api/v1/bookkeeping/emissions/factors |  |
| [**emissions_report_api**](EmissionsApi.md#emissions_report_api) | **GET** /api/v1/bookkeeping/emissions/report |  |
| [**emissions_targets_api**](EmissionsApi.md#emissions_targets_api) | **GET** /api/v1/bookkeeping/emissions/targets |  |


## create_emission_entry_api

> <EmissionEntry> create_emission_entry_api(create_emission_entry)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new
create_emission_entry = SimplebillyApi::CreateEmissionEntry.new({activity_value: 'activity_value_example', category_id: 'category_id_example', description: 'description_example', method: 'method_example', scope: 'scope_example', unit: 'unit_example', year: 37}) # CreateEmissionEntry | 

begin
  
  result = api_instance.create_emission_entry_api(create_emission_entry)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->create_emission_entry_api: #{e}"
end
```

#### Using the create_emission_entry_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EmissionEntry>, Integer, Hash)> create_emission_entry_api_with_http_info(create_emission_entry)

```ruby
begin
  
  data, status_code, headers = api_instance.create_emission_entry_api_with_http_info(create_emission_entry)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EmissionEntry>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->create_emission_entry_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_emission_entry** | [**CreateEmissionEntry**](CreateEmissionEntry.md) |  |  |

### Return type

[**EmissionEntry**](EmissionEntry.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_emission_target_api

> <EmissionTarget> create_emission_target_api(create_emission_target)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new
create_emission_target = SimplebillyApi::CreateEmissionTarget.new({base_value: 'base_value_example', base_year: 37, description: 'description_example', scope: 'scope_example', target_value: 'target_value_example', target_year: 37}) # CreateEmissionTarget | 

begin
  
  result = api_instance.create_emission_target_api(create_emission_target)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->create_emission_target_api: #{e}"
end
```

#### Using the create_emission_target_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EmissionTarget>, Integer, Hash)> create_emission_target_api_with_http_info(create_emission_target)

```ruby
begin
  
  data, status_code, headers = api_instance.create_emission_target_api_with_http_info(create_emission_target)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EmissionTarget>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->create_emission_target_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_emission_target** | [**CreateEmissionTarget**](CreateEmissionTarget.md) |  |  |

### Return type

[**EmissionTarget**](EmissionTarget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_emission_entry_api

> delete_emission_entry_api(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_emission_entry_api(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->delete_emission_entry_api: #{e}"
end
```

#### Using the delete_emission_entry_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_emission_entry_api_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_emission_entry_api_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->delete_emission_entry_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_emission_target_api

> delete_emission_target_api(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_emission_target_api(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->delete_emission_target_api: #{e}"
end
```

#### Using the delete_emission_target_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_emission_target_api_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_emission_target_api_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->delete_emission_target_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## emissions_entries_api

> <Array<EmissionEntry>> emissions_entries_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.emissions_entries_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_entries_api: #{e}"
end
```

#### Using the emissions_entries_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<EmissionEntry>>, Integer, Hash)> emissions_entries_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.emissions_entries_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<EmissionEntry>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_entries_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**Array&lt;EmissionEntry&gt;**](EmissionEntry.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## emissions_export_api

> <EmissionsExportResponse> emissions_export_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.emissions_export_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_export_api: #{e}"
end
```

#### Using the emissions_export_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EmissionsExportResponse>, Integer, Hash)> emissions_export_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.emissions_export_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EmissionsExportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_export_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**EmissionsExportResponse**](EmissionsExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## emissions_factors_api

> <Array<EmissionFactorResponse>> emissions_factors_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new

begin
  
  result = api_instance.emissions_factors_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_factors_api: #{e}"
end
```

#### Using the emissions_factors_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<EmissionFactorResponse>>, Integer, Hash)> emissions_factors_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.emissions_factors_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<EmissionFactorResponse>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_factors_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;EmissionFactorResponse&gt;**](EmissionFactorResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## emissions_report_api

> <EmissionsReport> emissions_report_api(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.emissions_report_api(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_report_api: #{e}"
end
```

#### Using the emissions_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EmissionsReport>, Integer, Hash)> emissions_report_api_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.emissions_report_api_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EmissionsReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**EmissionsReport**](EmissionsReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## emissions_targets_api

> <Array<EmissionTarget>> emissions_targets_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmissionsApi.new

begin
  
  result = api_instance.emissions_targets_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_targets_api: #{e}"
end
```

#### Using the emissions_targets_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<EmissionTarget>>, Integer, Hash)> emissions_targets_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.emissions_targets_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<EmissionTarget>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmissionsApi->emissions_targets_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;EmissionTarget&gt;**](EmissionTarget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

