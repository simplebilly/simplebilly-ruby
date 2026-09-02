# SimplebillyApi::PayrollApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**payroll_approve**](PayrollApi.md#payroll_approve) | **POST** /api/v1/payroll/{id}/approve |  |
| [**payroll_autopay**](PayrollApi.md#payroll_autopay) | **POST** /api/v1/payroll/{id}/autopay |  |
| [**payroll_calculate**](PayrollApi.md#payroll_calculate) | **POST** /api/v1/payroll/{id}/calculate |  |
| [**payroll_create**](PayrollApi.md#payroll_create) | **POST** /api/v1/payroll |  |
| [**payroll_delete**](PayrollApi.md#payroll_delete) | **DELETE** /api/v1/payroll/{id} |  |
| [**payroll_elster_export**](PayrollApi.md#payroll_elster_export) | **POST** /api/v1/payroll/{id}/elster-export |  |
| [**payroll_email**](PayrollApi.md#payroll_email) | **POST** /api/v1/payroll/{id}/email |  |
| [**payroll_entry_pdf**](PayrollApi.md#payroll_entry_pdf) | **GET** /api/v1/payroll/{id}/entries/{entry_id}/pdf |  |
| [**payroll_get**](PayrollApi.md#payroll_get) | **GET** /api/v1/payroll/{id} |  |
| [**payroll_list**](PayrollApi.md#payroll_list) | **GET** /api/v1/payroll |  |
| [**payroll_pay**](PayrollApi.md#payroll_pay) | **POST** /api/v1/payroll/{id}/pay |  |
| [**payroll_pdf**](PayrollApi.md#payroll_pdf) | **GET** /api/v1/payroll/{id}/pdf |  |
| [**payroll_summary**](PayrollApi.md#payroll_summary) | **GET** /api/v1/payroll/summary/{year} |  |
| [**payroll_sv_meldungen**](PayrollApi.md#payroll_sv_meldungen) | **POST** /api/v1/payroll/{id}/sv-meldungen |  |


## payroll_approve

> <PayrollRunApi> payroll_approve(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.payroll_approve(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_approve: #{e}"
end
```

#### Using the payroll_approve_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollRunApi>, Integer, Hash)> payroll_approve_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_approve_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollRunApi>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_approve_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payroll_autopay

> Object payroll_autopay(id, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = 'id_example' # String | 
opts = {
  body: 3.56 # Object | 
}

begin
  
  result = api_instance.payroll_autopay(id, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_autopay: #{e}"
end
```

#### Using the payroll_autopay_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> payroll_autopay_with_http_info(id, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_autopay_with_http_info(id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_autopay_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **body** | **Object** |  | [optional] |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## payroll_calculate

> <PayrollRunApi> payroll_calculate(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.payroll_calculate(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_calculate: #{e}"
end
```

#### Using the payroll_calculate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollRunApi>, Integer, Hash)> payroll_calculate_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_calculate_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollRunApi>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_calculate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payroll_create

> <PayrollRunApi> payroll_create(payroll_create_payload)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
payroll_create_payload = SimplebillyApi::PayrollCreatePayload.new({employee_ids: ['employee_ids_example'], month: 37, year: 37}) # PayrollCreatePayload | 

begin
  
  result = api_instance.payroll_create(payroll_create_payload)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_create: #{e}"
end
```

#### Using the payroll_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollRunApi>, Integer, Hash)> payroll_create_with_http_info(payroll_create_payload)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_create_with_http_info(payroll_create_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollRunApi>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payroll_create_payload** | [**PayrollCreatePayload**](PayrollCreatePayload.md) |  |  |

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## payroll_delete

> payroll_delete(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.payroll_delete(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_delete: #{e}"
end
```

#### Using the payroll_delete_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> payroll_delete_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_delete_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_delete_with_http_info: #{e}"
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
- **Accept**: Not defined


## payroll_elster_export

> payroll_elster_export(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.payroll_elster_export(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_elster_export: #{e}"
end
```

#### Using the payroll_elster_export_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> payroll_elster_export_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_elster_export_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_elster_export_with_http_info: #{e}"
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
- **Accept**: Not defined


## payroll_email

> Object payroll_email(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = 'id_example' # String | 

begin
  
  result = api_instance.payroll_email(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_email: #{e}"
end
```

#### Using the payroll_email_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> payroll_email_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_email_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_email_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payroll_entry_pdf

> payroll_entry_pdf(id, entry_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = 'id_example' # String | 
entry_id = 'entry_id_example' # String | 

begin
  
  api_instance.payroll_entry_pdf(id, entry_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_entry_pdf: #{e}"
end
```

#### Using the payroll_entry_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> payroll_entry_pdf_with_http_info(id, entry_id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_entry_pdf_with_http_info(id, entry_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_entry_pdf_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **entry_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf


## payroll_get

> <PayrollRunApi> payroll_get(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.payroll_get(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_get: #{e}"
end
```

#### Using the payroll_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollRunApi>, Integer, Hash)> payroll_get_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollRunApi>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payroll_list

> <Array<PayrollRunApi>> payroll_list(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
opts = {
  year: 56, # Integer | 
  status: 'status_example' # String | 
}

begin
  
  result = api_instance.payroll_list(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_list: #{e}"
end
```

#### Using the payroll_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PayrollRunApi>>, Integer, Hash)> payroll_list_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PayrollRunApi>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |

### Return type

[**Array&lt;PayrollRunApi&gt;**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payroll_pay

> <PayrollRunApi> payroll_pay(id, payroll_pay_payload)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
payroll_pay_payload = SimplebillyApi::PayrollPayPayload.new({payment_date: Date.today}) # PayrollPayPayload | 

begin
  
  result = api_instance.payroll_pay(id, payroll_pay_payload)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_pay: #{e}"
end
```

#### Using the payroll_pay_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollRunApi>, Integer, Hash)> payroll_pay_with_http_info(id, payroll_pay_payload)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_pay_with_http_info(id, payroll_pay_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollRunApi>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_pay_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **payroll_pay_payload** | [**PayrollPayPayload**](PayrollPayPayload.md) |  |  |

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## payroll_pdf

> payroll_pdf(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = 'id_example' # String | 

begin
  
  api_instance.payroll_pdf(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_pdf: #{e}"
end
```

#### Using the payroll_pdf_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> payroll_pdf_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_pdf_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_pdf_with_http_info: #{e}"
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
- **Accept**: application/pdf


## payroll_summary

> <YearlyPayrollSummary> payroll_summary(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.payroll_summary(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_summary: #{e}"
end
```

#### Using the payroll_summary_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<YearlyPayrollSummary>, Integer, Hash)> payroll_summary_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_summary_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <YearlyPayrollSummary>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_summary_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**YearlyPayrollSummary**](YearlyPayrollSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payroll_sv_meldungen

> Object payroll_sv_meldungen(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PayrollApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.payroll_sv_meldungen(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_sv_meldungen: #{e}"
end
```

#### Using the payroll_sv_meldungen_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> payroll_sv_meldungen_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.payroll_sv_meldungen_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PayrollApi->payroll_sv_meldungen_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

