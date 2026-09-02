# SimplebillyApi::TaxApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_tax_rate**](TaxApi.md#create_tax_rate) | **POST** /api/v1/tax-rates | Create a tax rate (&#x60;admin:settings&#x60;). |
| [**delete_tax_rate**](TaxApi.md#delete_tax_rate) | **DELETE** /api/v1/tax-rates/{id} | Delete a tax rate by id (&#x60;admin:settings&#x60;). |
| [**list_tax_rates**](TaxApi.md#list_tax_rates) | **GET** /api/v1/tax-rates | List the calling tenant&#39;s tax rates. |
| [**update_tax_rate**](TaxApi.md#update_tax_rate) | **PUT** /api/v1/tax-rates/{id} | Update a tax rate by id (&#x60;admin:settings&#x60;). Replaces all body fields. |


## create_tax_rate

> create_tax_rate(tax_rate_create)

Create a tax rate (`admin:settings`).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TaxApi.new
tax_rate_create = SimplebillyApi::TaxRateCreate.new({country_code: 'country_code_example', is_default: false, name: 'name_example', rate_percent: 3.56}) # TaxRateCreate | 

begin
  # Create a tax rate (`admin:settings`).
  api_instance.create_tax_rate(tax_rate_create)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->create_tax_rate: #{e}"
end
```

#### Using the create_tax_rate_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> create_tax_rate_with_http_info(tax_rate_create)

```ruby
begin
  # Create a tax rate (`admin:settings`).
  data, status_code, headers = api_instance.create_tax_rate_with_http_info(tax_rate_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->create_tax_rate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tax_rate_create** | [**TaxRateCreate**](TaxRateCreate.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## delete_tax_rate

> delete_tax_rate(id)

Delete a tax rate by id (`admin:settings`).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TaxApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Delete a tax rate by id (`admin:settings`).
  api_instance.delete_tax_rate(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->delete_tax_rate: #{e}"
end
```

#### Using the delete_tax_rate_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_tax_rate_with_http_info(id)

```ruby
begin
  # Delete a tax rate by id (`admin:settings`).
  data, status_code, headers = api_instance.delete_tax_rate_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->delete_tax_rate_with_http_info: #{e}"
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


## list_tax_rates

> list_tax_rates

List the calling tenant's tax rates.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TaxApi.new

begin
  # List the calling tenant's tax rates.
  api_instance.list_tax_rates
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->list_tax_rates: #{e}"
end
```

#### Using the list_tax_rates_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> list_tax_rates_with_http_info

```ruby
begin
  # List the calling tenant's tax rates.
  data, status_code, headers = api_instance.list_tax_rates_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->list_tax_rates_with_http_info: #{e}"
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


## update_tax_rate

> update_tax_rate(id, tax_rate_create)

Update a tax rate by id (`admin:settings`). Replaces all body fields.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TaxApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
tax_rate_create = SimplebillyApi::TaxRateCreate.new({country_code: 'country_code_example', is_default: false, name: 'name_example', rate_percent: 3.56}) # TaxRateCreate | 

begin
  # Update a tax rate by id (`admin:settings`). Replaces all body fields.
  api_instance.update_tax_rate(id, tax_rate_create)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->update_tax_rate: #{e}"
end
```

#### Using the update_tax_rate_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_tax_rate_with_http_info(id, tax_rate_create)

```ruby
begin
  # Update a tax rate by id (`admin:settings`). Replaces all body fields.
  data, status_code, headers = api_instance.update_tax_rate_with_http_info(id, tax_rate_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TaxApi->update_tax_rate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **tax_rate_create** | [**TaxRateCreate**](TaxRateCreate.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

