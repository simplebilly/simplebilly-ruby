# SimplebillyApi::WorkflowsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_workflows_api**](WorkflowsApi.md#list_workflows_api) | **GET** /api/v1/workflows |  |
| [**set_workflow_enabled_api**](WorkflowsApi.md#set_workflow_enabled_api) | **PUT** /api/v1/workflows/{workflow_id}/enabled |  |


## list_workflows_api

> <Array<Workflow>> list_workflows_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WorkflowsApi.new

begin
  
  result = api_instance.list_workflows_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WorkflowsApi->list_workflows_api: #{e}"
end
```

#### Using the list_workflows_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Workflow>>, Integer, Hash)> list_workflows_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_workflows_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Workflow>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WorkflowsApi->list_workflows_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;Workflow&gt;**](Workflow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## set_workflow_enabled_api

> <Workflow> set_workflow_enabled_api(workflow_id, workflow_enabled_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::WorkflowsApi.new
workflow_id = 'workflow_id_example' # String | 
workflow_enabled_update = SimplebillyApi::WorkflowEnabledUpdate.new({enabled: false}) # WorkflowEnabledUpdate | 

begin
  
  result = api_instance.set_workflow_enabled_api(workflow_id, workflow_enabled_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WorkflowsApi->set_workflow_enabled_api: #{e}"
end
```

#### Using the set_workflow_enabled_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Workflow>, Integer, Hash)> set_workflow_enabled_api_with_http_info(workflow_id, workflow_enabled_update)

```ruby
begin
  
  data, status_code, headers = api_instance.set_workflow_enabled_api_with_http_info(workflow_id, workflow_enabled_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Workflow>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling WorkflowsApi->set_workflow_enabled_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workflow_id** | **String** |  |  |
| **workflow_enabled_update** | [**WorkflowEnabledUpdate**](WorkflowEnabledUpdate.md) |  |  |

### Return type

[**Workflow**](Workflow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

