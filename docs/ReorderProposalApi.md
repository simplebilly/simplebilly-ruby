# SimplebillyApi::ReorderProposalApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**apply_reorder_proposal**](ReorderProposalApi.md#apply_reorder_proposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order. |
| [**get_reorder_proposal**](ReorderProposalApi.md#get_reorder_proposal) | **GET** /api/v1/reorder-proposals |  |


## apply_reorder_proposal

> Object apply_reorder_proposal(opts)

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReorderProposalApi.new
opts = {
  configured_only: true, # Boolean | Only include products with a reorder point configured (`min_stock`).
  warehouse_id: 'warehouse_id_example' # String | Limit to a single warehouse id.
}

begin
  # Convert a reorder proposal into a draft purchase order.
  result = api_instance.apply_reorder_proposal(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReorderProposalApi->apply_reorder_proposal: #{e}"
end
```

#### Using the apply_reorder_proposal_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> apply_reorder_proposal_with_http_info(opts)

```ruby
begin
  # Convert a reorder proposal into a draft purchase order.
  data, status_code, headers = api_instance.apply_reorder_proposal_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReorderProposalApi->apply_reorder_proposal_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **configured_only** | **Boolean** | Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] |
| **warehouse_id** | **String** | Limit to a single warehouse id. | [optional] |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_reorder_proposal

> <ReorderProposalResponse> get_reorder_proposal(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReorderProposalApi.new
opts = {
  configured_only: true, # Boolean | Only include products with a reorder point configured (`min_stock`).
  warehouse_id: 'warehouse_id_example' # String | Limit to a single warehouse id.
}

begin
  
  result = api_instance.get_reorder_proposal(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReorderProposalApi->get_reorder_proposal: #{e}"
end
```

#### Using the get_reorder_proposal_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReorderProposalResponse>, Integer, Hash)> get_reorder_proposal_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_reorder_proposal_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReorderProposalResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReorderProposalApi->get_reorder_proposal_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **configured_only** | **Boolean** | Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] |
| **warehouse_id** | **String** | Limit to a single warehouse id. | [optional] |

### Return type

[**ReorderProposalResponse**](ReorderProposalResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

