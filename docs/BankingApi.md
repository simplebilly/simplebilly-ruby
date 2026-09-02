# SimplebillyApi::BankingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bank_lookup_api**](BankingApi.md#bank_lookup_api) | **GET** /api/v1/bookkeeping/banking/lookup |  |
| [**bank_transactions_api**](BankingApi.md#bank_transactions_api) | **GET** /api/v1/bookkeeping/banking/transactions |  |
| [**hebesatz_lookup_api**](BankingApi.md#hebesatz_lookup_api) | **GET** /api/v1/bookkeeping/hebesatz |  |


## bank_lookup_api

> <BankLookup> bank_lookup_api(iban)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BankingApi.new
iban = 'iban_example' # String | 

begin
  
  result = api_instance.bank_lookup_api(iban)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BankingApi->bank_lookup_api: #{e}"
end
```

#### Using the bank_lookup_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BankLookup>, Integer, Hash)> bank_lookup_api_with_http_info(iban)

```ruby
begin
  
  data, status_code, headers = api_instance.bank_lookup_api_with_http_info(iban)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BankLookup>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BankingApi->bank_lookup_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **iban** | **String** |  |  |

### Return type

[**BankLookup**](BankLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## bank_transactions_api

> bank_transactions_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BankingApi.new

begin
  
  api_instance.bank_transactions_api
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BankingApi->bank_transactions_api: #{e}"
end
```

#### Using the bank_transactions_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> bank_transactions_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.bank_transactions_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BankingApi->bank_transactions_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## hebesatz_lookup_api

> <Array<HebesatzLookup>> hebesatz_lookup_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BankingApi.new
opts = {
  gemeindeschluessel: 'gemeindeschluessel_example', # String | 
  plz: 'plz_example', # String | 
  name: 'name_example', # String | 
  stichtag: 'stichtag_example', # String | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from <= date <= valid_to.
  country_code: 'country_code_example' # String | 
}

begin
  
  result = api_instance.hebesatz_lookup_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BankingApi->hebesatz_lookup_api: #{e}"
end
```

#### Using the hebesatz_lookup_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<HebesatzLookup>>, Integer, Hash)> hebesatz_lookup_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.hebesatz_lookup_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<HebesatzLookup>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BankingApi->hebesatz_lookup_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gemeindeschluessel** | **String** |  | [optional] |
| **plz** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **stichtag** | **String** | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from &lt;&#x3D; date &lt;&#x3D; valid_to. | [optional] |
| **country_code** | **String** |  | [optional] |

### Return type

[**Array&lt;HebesatzLookup&gt;**](HebesatzLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

