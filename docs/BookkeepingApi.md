# SimplebillyApi::BookkeepingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**allocate_payment_api**](BookkeepingApi.md#allocate_payment_api) | **POST** /api/v1/payments/allocate | Allocate a payment to an invoice |
| [**bwa_report_api**](BookkeepingApi.md#bwa_report_api) | **GET** /api/v1/bookkeeping/bwa | Get BWA (Betriebswirtschaftliche Auswertung) report |
| [**elster_status_api**](BookkeepingApi.md#elster_status_api) | **GET** /api/v1/bookkeeping/elster/status |  |
| [**elster_validate_api**](BookkeepingApi.md#elster_validate_api) | **POST** /api/v1/bookkeeping/ustva/elster-validate |  |
| [**elster_xml_api**](BookkeepingApi.md#elster_xml_api) | **GET** /api/v1/bookkeeping/ustva/elster-xml |  |
| [**get_cashflow**](BookkeepingApi.md#get_cashflow) | **GET** /api/v1/bookkeeping/cashflow | GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period. |
| [**get_liquidity**](BookkeepingApi.md#get_liquidity) | **GET** /api/v1/bookkeeping/liquidity | GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios. |
| [**get_open_invoices_api**](BookkeepingApi.md#get_open_invoices_api) | **GET** /api/v1/payments/open-invoices/{customer_id} | Get open invoices for a customer |
| [**get_verfahrensdokumentation**](BookkeepingApi.md#get_verfahrensdokumentation) | **GET** /api/v1/bookkeeping/verfahrensdokumentation | GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules. |
| [**run_dunning_api**](BookkeepingApi.md#run_dunning_api) | **POST** /api/v1/bookkeeping/dunning |  |


## allocate_payment_api

> allocate_payment_api(allocate_payment_request)

Allocate a payment to an invoice

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new
allocate_payment_request = SimplebillyApi::AllocatePaymentRequest.new({amount: 3.56, invoice_id: 'invoice_id_example', payment_id: 'payment_id_example'}) # AllocatePaymentRequest | 

begin
  # Allocate a payment to an invoice
  api_instance.allocate_payment_api(allocate_payment_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->allocate_payment_api: #{e}"
end
```

#### Using the allocate_payment_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> allocate_payment_api_with_http_info(allocate_payment_request)

```ruby
begin
  # Allocate a payment to an invoice
  data, status_code, headers = api_instance.allocate_payment_api_with_http_info(allocate_payment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->allocate_payment_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **allocate_payment_request** | [**AllocatePaymentRequest**](AllocatePaymentRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## bwa_report_api

> <BWAReport> bwa_report_api(opts)

Get BWA (Betriebswirtschaftliche Auswertung) report

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new
opts = {
  year: 56, # Integer | 
  month: 56 # Integer | 
}

begin
  # Get BWA (Betriebswirtschaftliche Auswertung) report
  result = api_instance.bwa_report_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->bwa_report_api: #{e}"
end
```

#### Using the bwa_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BWAReport>, Integer, Hash)> bwa_report_api_with_http_info(opts)

```ruby
begin
  # Get BWA (Betriebswirtschaftliche Auswertung) report
  data, status_code, headers = api_instance.bwa_report_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BWAReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->bwa_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **month** | **Integer** |  | [optional] |

### Return type

[**BWAReport**](BWAReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## elster_status_api

> <ElsterStatus> elster_status_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new

begin
  
  result = api_instance.elster_status_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->elster_status_api: #{e}"
end
```

#### Using the elster_status_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ElsterStatus>, Integer, Hash)> elster_status_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.elster_status_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ElsterStatus>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->elster_status_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ElsterStatus**](ElsterStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## elster_validate_api

> elster_validate_api(zeitraum)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new
zeitraum = 'zeitraum_example' # String | 

begin
  
  api_instance.elster_validate_api(zeitraum)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->elster_validate_api: #{e}"
end
```

#### Using the elster_validate_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> elster_validate_api_with_http_info(zeitraum)

```ruby
begin
  
  data, status_code, headers = api_instance.elster_validate_api_with_http_info(zeitraum)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->elster_validate_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **zeitraum** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## elster_xml_api

> elster_xml_api(zeitraum)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new
zeitraum = 'zeitraum_example' # String | 

begin
  
  api_instance.elster_xml_api(zeitraum)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->elster_xml_api: #{e}"
end
```

#### Using the elster_xml_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> elster_xml_api_with_http_info(zeitraum)

```ruby
begin
  
  data, status_code, headers = api_instance.elster_xml_api_with_http_info(zeitraum)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->elster_xml_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **zeitraum** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_cashflow

> <CashflowReport> get_cashflow(opts)

GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new
opts = {
  year: 56, # Integer | 
  month: 56 # Integer | 
}

begin
  # GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
  result = api_instance.get_cashflow(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_cashflow: #{e}"
end
```

#### Using the get_cashflow_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CashflowReport>, Integer, Hash)> get_cashflow_with_http_info(opts)

```ruby
begin
  # GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
  data, status_code, headers = api_instance.get_cashflow_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CashflowReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_cashflow_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **month** | **Integer** |  | [optional] |

### Return type

[**CashflowReport**](CashflowReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_liquidity

> <LiquidityPosition> get_liquidity

GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new

begin
  # GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
  result = api_instance.get_liquidity
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_liquidity: #{e}"
end
```

#### Using the get_liquidity_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LiquidityPosition>, Integer, Hash)> get_liquidity_with_http_info

```ruby
begin
  # GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
  data, status_code, headers = api_instance.get_liquidity_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LiquidityPosition>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_liquidity_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**LiquidityPosition**](LiquidityPosition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_open_invoices_api

> <Array<Invoice>> get_open_invoices_api(customer_id)

Get open invoices for a customer

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new
customer_id = 'customer_id_example' # String | 

begin
  # Get open invoices for a customer
  result = api_instance.get_open_invoices_api(customer_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_open_invoices_api: #{e}"
end
```

#### Using the get_open_invoices_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Invoice>>, Integer, Hash)> get_open_invoices_api_with_http_info(customer_id)

```ruby
begin
  # Get open invoices for a customer
  data, status_code, headers = api_instance.get_open_invoices_api_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Invoice>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_open_invoices_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |

### Return type

[**Array&lt;Invoice&gt;**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_verfahrensdokumentation

> <Verfahrensdokumentation> get_verfahrensdokumentation

GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new

begin
  # GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
  result = api_instance.get_verfahrensdokumentation
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_verfahrensdokumentation: #{e}"
end
```

#### Using the get_verfahrensdokumentation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Verfahrensdokumentation>, Integer, Hash)> get_verfahrensdokumentation_with_http_info

```ruby
begin
  # GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
  data, status_code, headers = api_instance.get_verfahrensdokumentation_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Verfahrensdokumentation>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->get_verfahrensdokumentation_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Verfahrensdokumentation**](Verfahrensdokumentation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## run_dunning_api

> <DunningResult> run_dunning_api



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BookkeepingApi.new

begin
  
  result = api_instance.run_dunning_api
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->run_dunning_api: #{e}"
end
```

#### Using the run_dunning_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DunningResult>, Integer, Hash)> run_dunning_api_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.run_dunning_api_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DunningResult>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BookkeepingApi->run_dunning_api_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**DunningResult**](DunningResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

