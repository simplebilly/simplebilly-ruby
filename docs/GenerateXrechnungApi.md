# SimplebillyApi::GenerateXrechnungApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_xrechnung_api**](GenerateXrechnungApi.md#generate_xrechnung_api) | **GET** /api/v1/invoices/{id}/xrechnung |  |


## generate_xrechnung_api

> <XRechnungResponse> generate_xrechnung_api(id, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GenerateXrechnungApi.new
id = 'id_example' # String | 
opts = {
  supplier_name: 'supplier_name_example', # String | 
  supplier_street: 'supplier_street_example', # String | 
  supplier_city: 'supplier_city_example', # String | 
  supplier_zip: 'supplier_zip_example', # String | 
  supplier_country: 'supplier_country_example', # String | 
  supplier_vat_id: 'supplier_vat_id_example' # String | 
}

begin
  
  result = api_instance.generate_xrechnung_api(id, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GenerateXrechnungApi->generate_xrechnung_api: #{e}"
end
```

#### Using the generate_xrechnung_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<XRechnungResponse>, Integer, Hash)> generate_xrechnung_api_with_http_info(id, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.generate_xrechnung_api_with_http_info(id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <XRechnungResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GenerateXrechnungApi->generate_xrechnung_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **supplier_name** | **String** |  | [optional] |
| **supplier_street** | **String** |  | [optional] |
| **supplier_city** | **String** |  | [optional] |
| **supplier_zip** | **String** |  | [optional] |
| **supplier_country** | **String** |  | [optional] |
| **supplier_vat_id** | **String** |  | [optional] |

### Return type

[**XRechnungResponse**](XRechnungResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

