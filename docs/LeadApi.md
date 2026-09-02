# SimplebillyApi::LeadApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_leads_api**](LeadApi.md#list_leads_api) | **GET** /api/v1/support/leads |  |
| [**update_lead_api**](LeadApi.md#update_lead_api) | **PUT** /api/v1/support/leads/{lead_id} |  |


## list_leads_api

> <Array<Lead>> list_leads_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::LeadApi.new
opts = {
  status: 'status_example', # String | 
  source: 'source_example', # String | 
  search: 'search_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  
  result = api_instance.list_leads_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LeadApi->list_leads_api: #{e}"
end
```

#### Using the list_leads_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Lead>>, Integer, Hash)> list_leads_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_leads_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Lead>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LeadApi->list_leads_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **source** | **String** |  | [optional] |
| **search** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**Array&lt;Lead&gt;**](Lead.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_lead_api

> <Lead> update_lead_api(lead_id, lead_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::LeadApi.new
lead_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
lead_update = SimplebillyApi::LeadUpdate.new # LeadUpdate | 

begin
  
  result = api_instance.update_lead_api(lead_id, lead_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LeadApi->update_lead_api: #{e}"
end
```

#### Using the update_lead_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Lead>, Integer, Hash)> update_lead_api_with_http_info(lead_id, lead_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_lead_api_with_http_info(lead_id, lead_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Lead>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling LeadApi->update_lead_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **lead_id** | **String** |  |  |
| **lead_update** | [**LeadUpdate**](LeadUpdate.md) |  |  |

### Return type

[**Lead**](Lead.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

