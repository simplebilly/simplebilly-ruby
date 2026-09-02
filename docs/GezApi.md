# SimplebillyApi::GezApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**gez_api**](GezApi.md#gez_api) | **GET** /api/v1/bookkeeping/gez |  |


## gez_api

> <GezReport> gez_api(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GezApi.new
opts = {
  jahr: 56, # Integer | 
  betriebsstaetten: 'betriebsstaetten_example', # String | Liste der Betriebsstätten als JSON, z.B. `[{\"name\":\"Filiale 1\",\"beschaefigte\":12}]`.
  kfz: 789, # Integer | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind).
  hotelzimmer: 789, # Integer | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen.
  beschaefigte: 789 # Integer | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen).
}

begin
  
  result = api_instance.gez_api(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GezApi->gez_api: #{e}"
end
```

#### Using the gez_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GezReport>, Integer, Hash)> gez_api_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.gez_api_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GezReport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GezApi->gez_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **jahr** | **Integer** |  | [optional] |
| **betriebsstaetten** | **String** | Liste der Betriebsstätten als JSON, z.B. &#x60;[{\&quot;name\&quot;:\&quot;Filiale 1\&quot;,\&quot;beschaefigte\&quot;:12}]&#x60;. | [optional] |
| **kfz** | **Integer** | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional] |
| **hotelzimmer** | **Integer** | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional] |
| **beschaefigte** | **Integer** | Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional] |

### Return type

[**GezReport**](GezReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

