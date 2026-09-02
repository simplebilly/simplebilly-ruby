# SimplebillyApi::EmailTemplateApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_email_template**](EmailTemplateApi.md#create_email_template) | **POST** /api/v1/email-templates |  |
| [**delete_email_template**](EmailTemplateApi.md#delete_email_template) | **DELETE** /api/v1/email-templates/{email_template_id} |  |
| [**get_email_template**](EmailTemplateApi.md#get_email_template) | **GET** /api/v1/email-templates/{email_template_id} |  |
| [**list_email_templates**](EmailTemplateApi.md#list_email_templates) | **GET** /api/v1/email-templates/ |  |
| [**render_email_template**](EmailTemplateApi.md#render_email_template) | **POST** /api/v1/email-templates/{email_template_id}/render |  |
| [**update_email_template**](EmailTemplateApi.md#update_email_template) | **PUT** /api/v1/email-templates/{email_template_id} |  |


## create_email_template

> <EmailTemplate> create_email_template(email_template_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmailTemplateApi.new
email_template_create = SimplebillyApi::EmailTemplateCreate.new({body: 'body_example', name: 'name_example', status: SimplebillyApi::EmailTemplateStatus::ACTIVE, subject: 'subject_example'}) # EmailTemplateCreate | 

begin
  
  result = api_instance.create_email_template(email_template_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->create_email_template: #{e}"
end
```

#### Using the create_email_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EmailTemplate>, Integer, Hash)> create_email_template_with_http_info(email_template_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_email_template_with_http_info(email_template_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EmailTemplate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->create_email_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email_template_create** | [**EmailTemplateCreate**](EmailTemplateCreate.md) |  |  |

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_email_template

> delete_email_template(email_template_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmailTemplateApi.new
email_template_id = 'email_template_id_example' # String | 

begin
  
  api_instance.delete_email_template(email_template_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->delete_email_template: #{e}"
end
```

#### Using the delete_email_template_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_email_template_with_http_info(email_template_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_email_template_with_http_info(email_template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->delete_email_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email_template_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_email_template

> <EmailTemplate> get_email_template(email_template_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmailTemplateApi.new
email_template_id = 'email_template_id_example' # String | 

begin
  
  result = api_instance.get_email_template(email_template_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->get_email_template: #{e}"
end
```

#### Using the get_email_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EmailTemplate>, Integer, Hash)> get_email_template_with_http_info(email_template_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_email_template_with_http_info(email_template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EmailTemplate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->get_email_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email_template_id** | **String** |  |  |

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_email_templates

> <Array<EmailTemplate>> list_email_templates(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmailTemplateApi.new
opts = {
  page: 56, # Integer | 
  page_size: 56, # Integer | 
  status: 'status_example', # String | 
  search: 'search_example' # String | 
}

begin
  
  result = api_instance.list_email_templates(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->list_email_templates: #{e}"
end
```

#### Using the list_email_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<EmailTemplate>>, Integer, Hash)> list_email_templates_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_email_templates_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<EmailTemplate>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->list_email_templates_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **search** | **String** |  | [optional] |

### Return type

[**Array&lt;EmailTemplate&gt;**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## render_email_template

> Object render_email_template(email_template_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmailTemplateApi.new
email_template_id = 'email_template_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.render_email_template(email_template_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->render_email_template: #{e}"
end
```

#### Using the render_email_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> render_email_template_with_http_info(email_template_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.render_email_template_with_http_info(email_template_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->render_email_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email_template_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_email_template

> <EmailTemplate> update_email_template(email_template_id, email_template_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::EmailTemplateApi.new
email_template_id = 'email_template_id_example' # String | 
email_template_update = SimplebillyApi::EmailTemplateUpdate.new # EmailTemplateUpdate | 

begin
  
  result = api_instance.update_email_template(email_template_id, email_template_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->update_email_template: #{e}"
end
```

#### Using the update_email_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<EmailTemplate>, Integer, Hash)> update_email_template_with_http_info(email_template_id, email_template_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_email_template_with_http_info(email_template_id, email_template_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <EmailTemplate>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling EmailTemplateApi->update_email_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email_template_id** | **String** |  |  |
| **email_template_update** | [**EmailTemplateUpdate**](EmailTemplateUpdate.md) |  |  |

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

