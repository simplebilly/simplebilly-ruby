# SimplebillyApi::GenerateQrcodeApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_qrcode_api**](GenerateQrcodeApi.md#generate_qrcode_api) | **GET** /api/v1/invoices/{id}/qrcode |  |


## generate_qrcode_api

> <QRCodeResponse> generate_qrcode_api(iban, id, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GenerateQrcodeApi.new
iban = 'iban_example' # String | 
id = 'id_example' # String | 
opts = {
  holder_name: 'holder_name_example', # String | 
  bic: 'bic_example', # String | 
  amount: 'amount_example', # String | 
  reference: 'reference_example', # String | 
  purpose: 'purpose_example' # String | 
}

begin
  
  result = api_instance.generate_qrcode_api(iban, id, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GenerateQrcodeApi->generate_qrcode_api: #{e}"
end
```

#### Using the generate_qrcode_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<QRCodeResponse>, Integer, Hash)> generate_qrcode_api_with_http_info(iban, id, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.generate_qrcode_api_with_http_info(iban, id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <QRCodeResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GenerateQrcodeApi->generate_qrcode_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **iban** | **String** |  |  |
| **id** | **String** |  |  |
| **holder_name** | **String** |  | [optional] |
| **bic** | **String** |  | [optional] |
| **amount** | **String** |  | [optional] |
| **reference** | **String** |  | [optional] |
| **purpose** | **String** |  | [optional] |

### Return type

[**QRCodeResponse**](QRCodeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

