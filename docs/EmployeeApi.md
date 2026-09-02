# SimplebillyApi::EmployeeApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_employee**](EmployeeApi.md#create_employee) | **POST** /api/v1/employees |  |
| [**delete_employee**](EmployeeApi.md#delete_employee) | **DELETE** /api/v1/employees/{id} |  |
| [**employee_restore**](EmployeeApi.md#employee_restore) | **POST** /api/v1/employees/{id}/restore |  |
| [**get_employee**](EmployeeApi.md#get_employee) | **GET** /api/v1/employees/{id} |  |
| [**get_employee_payroll_summary**](EmployeeApi.md#get_employee_payroll_summary) | **GET** /api/v1/employees/{id}/payroll-summary |  |
| [**get_employees**](EmployeeApi.md#get_employees) | **GET** /api/v1/employees/ |  |
| [**update_employee**](EmployeeApi.md#update_employee) | **PUT** /api/v1/employees/{id} |  |


## create_employee

> <Employee> create_employee(employee_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmployeeApi.new
employee_create = SimplebillyApi::EmployeeCreate.new # EmployeeCreate | 

begin
  
  result = api_instance.create_employee(employee_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->create_employee: #{e}"
end
```

#### Using the create_employee_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Employee>, Integer, Hash)> create_employee_with_http_info(employee_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_employee_with_http_info(employee_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Employee>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->create_employee_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **employee_create** | [**EmployeeCreate**](EmployeeCreate.md) |  |  |

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_employee

> delete_employee(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmployeeApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_employee(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->delete_employee: #{e}"
end
```

#### Using the delete_employee_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_employee_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_employee_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->delete_employee_with_http_info: #{e}"
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
- **Accept**: application/json


## employee_restore

> <Employee> employee_restore(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmployeeApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.employee_restore(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->employee_restore: #{e}"
end
```

#### Using the employee_restore_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Employee>, Integer, Hash)> employee_restore_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.employee_restore_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Employee>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->employee_restore_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_employee

> <Employee> get_employee(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmployeeApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_employee(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->get_employee: #{e}"
end
```

#### Using the get_employee_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Employee>, Integer, Hash)> get_employee_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_employee_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Employee>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->get_employee_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_employee_payroll_summary

> <PayrollSummary> get_employee_payroll_summary(id, opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmployeeApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
opts = {
  year: 56 # Integer | Fiscal year for the breakdown; defaults to the current year.
}

begin
  
  result = api_instance.get_employee_payroll_summary(id, opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->get_employee_payroll_summary: #{e}"
end
```

#### Using the get_employee_payroll_summary_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollSummary>, Integer, Hash)> get_employee_payroll_summary_with_http_info(id, opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_employee_payroll_summary_with_http_info(id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollSummary>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->get_employee_payroll_summary_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **year** | **Integer** | Fiscal year for the breakdown; defaults to the current year. | [optional] |

### Return type

[**PayrollSummary**](PayrollSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_employees

> <Array<Employee>> get_employees(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmployeeApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_employees(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->get_employees: #{e}"
end
```

#### Using the get_employees_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Employee>>, Integer, Hash)> get_employees_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_employees_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Employee>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->get_employees_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **search** | **String** |  | [optional] |
| **include_deleted** | **Boolean** | Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] |

### Return type

[**Array&lt;Employee&gt;**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_employee

> <Employee> update_employee(id, employee_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmployeeApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
employee_update = SimplebillyApi::EmployeeUpdate.new # EmployeeUpdate | 

begin
  
  result = api_instance.update_employee(id, employee_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->update_employee: #{e}"
end
```

#### Using the update_employee_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Employee>, Integer, Hash)> update_employee_with_http_info(id, employee_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_employee_with_http_info(id, employee_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Employee>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmployeeApi->update_employee_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **employee_update** | [**EmployeeUpdate**](EmployeeUpdate.md) |  |  |

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

