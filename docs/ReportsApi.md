# SimplebillyApi::ReportsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bilanz_report_api**](ReportsApi.md#bilanz_report_api) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet) |
| [**guv_report_api**](ReportsApi.md#guv_report_api) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement) |
| [**kontenansicht_report_api**](ReportsApi.md#kontenansicht_report_api) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview) |
| [**umsatzsteuer_report_api**](ReportsApi.md#umsatzsteuer_report_api) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report) |


## bilanz_report_api

> <BilanzReport> bilanz_report_api(opts)

Bilanz (Balance Sheet)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReportsApi.new
opts = {
  year: 56, # Integer | 
  month: 56, # Integer | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # Bilanz (Balance Sheet)
  result = api_instance.bilanz_report_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->bilanz_report_api: #{e}"
end
```

#### Using the bilanz_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BilanzReport>, Integer, Hash)> bilanz_report_api_with_http_info(opts)

```ruby
begin
  # Bilanz (Balance Sheet)
  data, status_code, headers = api_instance.bilanz_report_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BilanzReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->bilanz_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **month** | **Integer** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**BilanzReport**](BilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## guv_report_api

> <GuVReport> guv_report_api(opts)

Gewinn- und Verlustrechnung (P&L statement)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReportsApi.new
opts = {
  year: 56, # Integer | 
  month: 56, # Integer | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # Gewinn- und Verlustrechnung (P&L statement)
  result = api_instance.guv_report_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->guv_report_api: #{e}"
end
```

#### Using the guv_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GuVReport>, Integer, Hash)> guv_report_api_with_http_info(opts)

```ruby
begin
  # Gewinn- und Verlustrechnung (P&L statement)
  data, status_code, headers = api_instance.guv_report_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GuVReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->guv_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **month** | **Integer** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**GuVReport**](GuVReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## kontenansicht_report_api

> <KontoReport> kontenansicht_report_api(opts)

Kontenansicht (Account Overview)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReportsApi.new
opts = {
  year: 56, # Integer | 
  month: 56, # Integer | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # Kontenansicht (Account Overview)
  result = api_instance.kontenansicht_report_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->kontenansicht_report_api: #{e}"
end
```

#### Using the kontenansicht_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<KontoReport>, Integer, Hash)> kontenansicht_report_api_with_http_info(opts)

```ruby
begin
  # Kontenansicht (Account Overview)
  data, status_code, headers = api_instance.kontenansicht_report_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <KontoReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->kontenansicht_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **month** | **Integer** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**KontoReport**](KontoReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## umsatzsteuer_report_api

> <UmsatzsteuerReport> umsatzsteuer_report_api(opts)

Umsatzsteuer-Voranmeldung (VAT report)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::ReportsApi.new
opts = {
  year: 56, # Integer | 
  month: 56, # Integer | 
  date_from: 'date_from_example', # String | 
  date_to: 'date_to_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  # Umsatzsteuer-Voranmeldung (VAT report)
  result = api_instance.umsatzsteuer_report_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->umsatzsteuer_report_api: #{e}"
end
```

#### Using the umsatzsteuer_report_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UmsatzsteuerReport>, Integer, Hash)> umsatzsteuer_report_api_with_http_info(opts)

```ruby
begin
  # Umsatzsteuer-Voranmeldung (VAT report)
  data, status_code, headers = api_instance.umsatzsteuer_report_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UmsatzsteuerReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling ReportsApi->umsatzsteuer_report_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  | [optional] |
| **month** | **Integer** |  | [optional] |
| **date_from** | **String** |  | [optional] |
| **date_to** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**UmsatzsteuerReport**](UmsatzsteuerReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

