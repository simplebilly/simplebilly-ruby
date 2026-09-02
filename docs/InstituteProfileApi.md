# SimplebillyApi::InstituteProfileApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_institute_profile**](InstituteProfileApi.md#get_institute_profile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing). |
| [**update_institute_profile**](InstituteProfileApi.md#update_institute_profile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert). |


## get_institute_profile

> <InstituteProfile> get_institute_profile

Current institute profile (created with defaults when missing).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InstituteProfileApi.new

begin
  # Current institute profile (created with defaults when missing).
  result = api_instance.get_institute_profile
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InstituteProfileApi->get_institute_profile: #{e}"
end
```

#### Using the get_institute_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InstituteProfile>, Integer, Hash)> get_institute_profile_with_http_info

```ruby
begin
  # Current institute profile (created with defaults when missing).
  data, status_code, headers = api_instance.get_institute_profile_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InstituteProfile>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InstituteProfileApi->get_institute_profile_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_institute_profile

> <InstituteProfile> update_institute_profile(institute_profile_update)

Update the institute profile (institute_type and/or kapitalmarktorientiert).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::InstituteProfileApi.new
institute_profile_update = SimplebillyApi::InstituteProfileUpdate.new # InstituteProfileUpdate | 

begin
  # Update the institute profile (institute_type and/or kapitalmarktorientiert).
  result = api_instance.update_institute_profile(institute_profile_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InstituteProfileApi->update_institute_profile: #{e}"
end
```

#### Using the update_institute_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InstituteProfile>, Integer, Hash)> update_institute_profile_with_http_info(institute_profile_update)

```ruby
begin
  # Update the institute profile (institute_type and/or kapitalmarktorientiert).
  data, status_code, headers = api_instance.update_institute_profile_with_http_info(institute_profile_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InstituteProfile>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling InstituteProfileApi->update_institute_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institute_profile_update** | [**InstituteProfileUpdate**](InstituteProfileUpdate.md) |  |  |

### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

