# SimplebillyApi::GobdExportApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**buchhalter_csv_api**](GobdExportApi.md#buchhalter_csv_api) | **GET** /api/v1/bookkeeping/buchhalter-csv |  |
| [**gobd_export_api**](GobdExportApi.md#gobd_export_api) | **GET** /api/v1/bookkeeping/gobd | GoBD/GDPdU export. Default: ZIP archive (&#x60;index.xml&#x60; + CSV tables, IDEA format). &#x60;?format&#x3D;csv&#x60; returns the legacy single-journal CSV as JSON. |


## buchhalter_csv_api

> <GoBDExportResponse> buchhalter_csv_api(date_from, date_to)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GobdExportApi.new
date_from = 'date_from_example' # String | 
date_to = 'date_to_example' # String | 

begin
  
  result = api_instance.buchhalter_csv_api(date_from, date_to)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GobdExportApi->buchhalter_csv_api: #{e}"
end
```

#### Using the buchhalter_csv_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GoBDExportResponse>, Integer, Hash)> buchhalter_csv_api_with_http_info(date_from, date_to)

```ruby
begin
  
  data, status_code, headers = api_instance.buchhalter_csv_api_with_http_info(date_from, date_to)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GoBDExportResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GobdExportApi->buchhalter_csv_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date_from** | **String** |  |  |
| **date_to** | **String** |  |  |

### Return type

[**GoBDExportResponse**](GoBDExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gobd_export_api

> gobd_export_api(year, opts)

GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GobdExportApi.new
year = 56 # Integer | 
opts = {
  format: 'zip' # String | Export format: `zip` (default, full GDPdU/IDEA export) or `csv` (legacy single-journal CSV as JSON).
}

begin
  # GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.
  api_instance.gobd_export_api(year, opts)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GobdExportApi->gobd_export_api: #{e}"
end
```

#### Using the gobd_export_api_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> gobd_export_api_with_http_info(year, opts)

```ruby
begin
  # GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.
  data, status_code, headers = api_instance.gobd_export_api_with_http_info(year, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GobdExportApi->gobd_export_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |
| **format** | **String** | Export format: &#x60;zip&#x60; (default, full GDPdU/IDEA export) or &#x60;csv&#x60; (legacy single-journal CSV as JSON). | [optional] |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json

