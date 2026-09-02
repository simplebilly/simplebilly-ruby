# SimplebillyApi::TimeEntriesApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**clock_in_time_entry**](TimeEntriesApi.md#clock_in_time_entry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile). |
| [**clock_out_time_entry**](TimeEntriesApi.md#clock_out_time_entry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;. |
| [**get_labor_costs**](TimeEntriesApi.md#get_labor_costs) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate. |
| [**list_time_entries**](TimeEntriesApi.md#list_time_entries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters. |


## clock_in_time_entry

> <TimeEntryDto> clock_in_time_entry(time_entry_clock_in)

Clock in for the authenticated user (resolved via their employee profile).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TimeEntriesApi.new
time_entry_clock_in = SimplebillyApi::TimeEntryClockIn.new # TimeEntryClockIn | 

begin
  # Clock in for the authenticated user (resolved via their employee profile).
  result = api_instance.clock_in_time_entry(time_entry_clock_in)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->clock_in_time_entry: #{e}"
end
```

#### Using the clock_in_time_entry_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TimeEntryDto>, Integer, Hash)> clock_in_time_entry_with_http_info(time_entry_clock_in)

```ruby
begin
  # Clock in for the authenticated user (resolved via their employee profile).
  data, status_code, headers = api_instance.clock_in_time_entry_with_http_info(time_entry_clock_in)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TimeEntryDto>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->clock_in_time_entry_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **time_entry_clock_in** | [**TimeEntryClockIn**](TimeEntryClockIn.md) |  |  |

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## clock_out_time_entry

> <TimeEntryDto> clock_out_time_entry(id, time_entry_clock_out)

Clock out an entry: the entry's owner, or anyone with `time_entries:write`.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TimeEntriesApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
time_entry_clock_out = SimplebillyApi::TimeEntryClockOut.new({clock_out: Time.now}) # TimeEntryClockOut | 

begin
  # Clock out an entry: the entry's owner, or anyone with `time_entries:write`.
  result = api_instance.clock_out_time_entry(id, time_entry_clock_out)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->clock_out_time_entry: #{e}"
end
```

#### Using the clock_out_time_entry_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TimeEntryDto>, Integer, Hash)> clock_out_time_entry_with_http_info(id, time_entry_clock_out)

```ruby
begin
  # Clock out an entry: the entry's owner, or anyone with `time_entries:write`.
  data, status_code, headers = api_instance.clock_out_time_entry_with_http_info(id, time_entry_clock_out)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TimeEntryDto>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->clock_out_time_entry_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **time_entry_clock_out** | [**TimeEntryClockOut**](TimeEntryClockOut.md) |  |  |

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_labor_costs

> <Array<LaborCostRow>> get_labor_costs(from, to, group_by)

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TimeEntriesApi.new
from = Date.parse('2013-10-20') # Date | 
to = Date.parse('2013-10-20') # Date | 
group_by = 'group_by_example' # String | One of \"employee\", \"order\" or \"day\".

begin
  # Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.
  result = api_instance.get_labor_costs(from, to, group_by)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->get_labor_costs: #{e}"
end
```

#### Using the get_labor_costs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<LaborCostRow>>, Integer, Hash)> get_labor_costs_with_http_info(from, to, group_by)

```ruby
begin
  # Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.
  data, status_code, headers = api_instance.get_labor_costs_with_http_info(from, to, group_by)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<LaborCostRow>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->get_labor_costs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **from** | **Date** |  |  |
| **to** | **Date** |  |  |
| **group_by** | **String** | One of \&quot;employee\&quot;, \&quot;order\&quot; or \&quot;day\&quot;. |  |

### Return type

[**Array&lt;LaborCostRow&gt;**](LaborCostRow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_time_entries

> <Array<TimeEntryDto>> list_time_entries(opts)

List time entries with optional date-range / active / employee filters.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::TimeEntriesApi.new
opts = {
  from: Date.parse('2013-10-20'), # Date | 
  to: Date.parse('2013-10-20'), # Date | 
  active: true, # Boolean | Only currently running shifts (clock_in set, clock_out null).
  employee_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
}

begin
  # List time entries with optional date-range / active / employee filters.
  result = api_instance.list_time_entries(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->list_time_entries: #{e}"
end
```

#### Using the list_time_entries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<TimeEntryDto>>, Integer, Hash)> list_time_entries_with_http_info(opts)

```ruby
begin
  # List time entries with optional date-range / active / employee filters.
  data, status_code, headers = api_instance.list_time_entries_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<TimeEntryDto>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling TimeEntriesApi->list_time_entries_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **from** | **Date** |  | [optional] |
| **to** | **Date** |  | [optional] |
| **active** | **Boolean** | Only currently running shifts (clock_in set, clock_out null). | [optional] |
| **employee_id** | **String** |  | [optional] |

### Return type

[**Array&lt;TimeEntryDto&gt;**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

