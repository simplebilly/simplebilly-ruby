# SimplebillyApi::RecurringTemplateApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_recurring_template**](RecurringTemplateApi.md#create_recurring_template) | **POST** /api/v1/recurring-templates |  |
| [**delete_recurring_template**](RecurringTemplateApi.md#delete_recurring_template) | **DELETE** /api/v1/recurring-templates/{template_id} |  |
| [**get_recurring_template**](RecurringTemplateApi.md#get_recurring_template) | **GET** /api/v1/recurring-templates/{template_id} |  |
| [**list_recurring_templates**](RecurringTemplateApi.md#list_recurring_templates) | **GET** /api/v1/recurring-templates/ |  |


## create_recurring_template

> <RecurringTemplate> create_recurring_template(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RecurringTemplateApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.create_recurring_template(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->create_recurring_template: #{e}"
end
```

#### Using the create_recurring_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringTemplate>, Integer, Hash)> create_recurring_template_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.create_recurring_template_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringTemplate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->create_recurring_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

[**RecurringTemplate**](RecurringTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_recurring_template

> delete_recurring_template(template_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RecurringTemplateApi.new
template_id = 'template_id_example' # String | 

begin
  
  api_instance.delete_recurring_template(template_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->delete_recurring_template: #{e}"
end
```

#### Using the delete_recurring_template_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_recurring_template_with_http_info(template_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_recurring_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->delete_recurring_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_recurring_template

> <RecurringTemplate> get_recurring_template(template_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RecurringTemplateApi.new
template_id = 'template_id_example' # String | 

begin
  
  result = api_instance.get_recurring_template(template_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->get_recurring_template: #{e}"
end
```

#### Using the get_recurring_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringTemplate>, Integer, Hash)> get_recurring_template_with_http_info(template_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_recurring_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringTemplate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->get_recurring_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

[**RecurringTemplate**](RecurringTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_recurring_templates

> <Array<RecurringTemplate>> list_recurring_templates



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::RecurringTemplateApi.new

begin
  
  result = api_instance.list_recurring_templates
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->list_recurring_templates: #{e}"
end
```

#### Using the list_recurring_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<RecurringTemplate>>, Integer, Hash)> list_recurring_templates_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_recurring_templates_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<RecurringTemplate>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling RecurringTemplateApi->list_recurring_templates_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;RecurringTemplate&gt;**](RecurringTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

