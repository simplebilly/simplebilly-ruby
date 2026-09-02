# SimplebillyApi::ProposeAssignmentsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**propose_assignments_api**](ProposeAssignmentsApi.md#propose_assignments_api) | **GET** /api/v1/bookkeeping/propose-assignments |  |


## propose_assignments_api

> <Array<ProposedAssignment>> propose_assignments_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ProposeAssignmentsApi.new
opts = {
  min_confidence: 1.2, # Float | 
  customer_id: 'customer_id_example' # String | 
}

begin
  
  result = api_instance.propose_assignments_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProposeAssignmentsApi->propose_assignments_api: #{e}"
end
```

#### Using the propose_assignments_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ProposedAssignment>>, Integer, Hash)> propose_assignments_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.propose_assignments_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ProposedAssignment>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ProposeAssignmentsApi->propose_assignments_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **min_confidence** | **Float** |  | [optional] |
| **customer_id** | **String** |  | [optional] |

### Return type

[**Array&lt;ProposedAssignment&gt;**](ProposedAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

