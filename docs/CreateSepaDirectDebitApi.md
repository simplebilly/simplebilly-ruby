# SimplebillyApi::CreateSepaDirectDebitApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_sepa_direct_debit_api**](CreateSepaDirectDebitApi.md#create_sepa_direct_debit_api) | **POST** /api/v1/bookkeeping/sepa-direct-debit |  |


## create_sepa_direct_debit_api

> <SepaDirectDebitResponse> create_sepa_direct_debit_api(creditor_name, creditor_iban, creditor_id, mandate_id, mandate_date, debtor_name, debtor_iban, amount, collection_date, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::CreateSepaDirectDebitApi.new
creditor_name = 'creditor_name_example' # String | 
creditor_iban = 'creditor_iban_example' # String | 
creditor_id = 'creditor_id_example' # String | 
mandate_id = 'mandate_id_example' # String | 
mandate_date = 'mandate_date_example' # String | 
debtor_name = 'debtor_name_example' # String | 
debtor_iban = 'debtor_iban_example' # String | 
amount = 'amount_example' # String | 
collection_date = 'collection_date_example' # String | 
opts = {
  creditor_bic: 'creditor_bic_example', # String | 
  debtor_bic: 'debtor_bic_example', # String | 
  description: 'description_example' # String | 
}

begin
  
  result = api_instance.create_sepa_direct_debit_api(creditor_name, creditor_iban, creditor_id, mandate_id, mandate_date, debtor_name, debtor_iban, amount, collection_date, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreateSepaDirectDebitApi->create_sepa_direct_debit_api: #{e}"
end
```

#### Using the create_sepa_direct_debit_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SepaDirectDebitResponse>, Integer, Hash)> create_sepa_direct_debit_api_with_http_info(creditor_name, creditor_iban, creditor_id, mandate_id, mandate_date, debtor_name, debtor_iban, amount, collection_date, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.create_sepa_direct_debit_api_with_http_info(creditor_name, creditor_iban, creditor_id, mandate_id, mandate_date, debtor_name, debtor_iban, amount, collection_date, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SepaDirectDebitResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling CreateSepaDirectDebitApi->create_sepa_direct_debit_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **creditor_name** | **String** |  |  |
| **creditor_iban** | **String** |  |  |
| **creditor_id** | **String** |  |  |
| **mandate_id** | **String** |  |  |
| **mandate_date** | **String** |  |  |
| **debtor_name** | **String** |  |  |
| **debtor_iban** | **String** |  |  |
| **amount** | **String** |  |  |
| **collection_date** | **String** |  |  |
| **creditor_bic** | **String** |  | [optional] |
| **debtor_bic** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |

### Return type

[**SepaDirectDebitResponse**](SepaDirectDebitResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

