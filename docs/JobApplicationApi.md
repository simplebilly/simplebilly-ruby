# SimplebillyApi::JobApplicationApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**apply_public**](JobApplicationApi.md#apply_public) | **POST** /api/v1/public/jobs/{posting_id}/apply |  |
| [**delete_job_application**](JobApplicationApi.md#delete_job_application) | **DELETE** /api/v1/job-applications/{application_id} |  |
| [**download_cv**](JobApplicationApi.md#download_cv) | **GET** /api/v1/job-applications/{application_id}/cv |  |
| [**get_job_application**](JobApplicationApi.md#get_job_application) | **GET** /api/v1/job-applications/{application_id} |  |
| [**inbound_email**](JobApplicationApi.md#inbound_email) | **POST** /api/v1/public/jobs/inbound-email | Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with &#x60;from&#x60;, &#x60;subject&#x60;, &#x60;body-plain&#x60; and one or more &#x60;attachment-N&#x60; file fields. The subject may reference a posting as &#x60;[JOB-&lt;posting_id&gt;]&#x60;; without one the application lands in the general inbox. |
| [**list_job_applications**](JobApplicationApi.md#list_job_applications) | **GET** /api/v1/job-applications |  |
| [**list_public_postings**](JobApplicationApi.md#list_public_postings) | **GET** /api/v1/public/jobs |  |
| [**score_job_application**](JobApplicationApi.md#score_job_application) | **POST** /api/v1/job-applications/{application_id}/score |  |
| [**update_job_application_status**](JobApplicationApi.md#update_job_application_status) | **PATCH** /api/v1/job-applications/{application_id}/status |  |


## apply_public

> apply_public(posting_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new
posting_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.apply_public(posting_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->apply_public: #{e}"
end
```

#### Using the apply_public_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> apply_public_with_http_info(posting_id)

```ruby
begin
  
  data, status_code, headers = api_instance.apply_public_with_http_info(posting_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->apply_public_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posting_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## delete_job_application

> <JobApplication> delete_job_application(application_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new
application_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.delete_job_application(application_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->delete_job_application: #{e}"
end
```

#### Using the delete_job_application_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobApplication>, Integer, Hash)> delete_job_application_with_http_info(application_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_job_application_with_http_info(application_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobApplication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->delete_job_application_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **application_id** | **String** |  |  |

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_cv

> download_cv(application_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new
application_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.download_cv(application_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->download_cv: #{e}"
end
```

#### Using the download_cv_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> download_cv_with_http_info(application_id)

```ruby
begin
  
  data, status_code, headers = api_instance.download_cv_with_http_info(application_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->download_cv_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **application_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_job_application

> <JobApplication> get_job_application(application_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new
application_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_job_application(application_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->get_job_application: #{e}"
end
```

#### Using the get_job_application_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobApplication>, Integer, Hash)> get_job_application_with_http_info(application_id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_job_application_with_http_info(application_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobApplication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->get_job_application_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **application_id** | **String** |  |  |

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## inbound_email

> inbound_email

Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new

begin
  # Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.
  api_instance.inbound_email
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->inbound_email: #{e}"
end
```

#### Using the inbound_email_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> inbound_email_with_http_info

```ruby
begin
  # Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.
  data, status_code, headers = api_instance.inbound_email_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->inbound_email_with_http_info: #{e}"
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


## list_job_applications

> <Array<JobApplication>> list_job_applications(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new
opts = {
  posting_id: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  status: 'status_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  
  result = api_instance.list_job_applications(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->list_job_applications: #{e}"
end
```

#### Using the list_job_applications_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<JobApplication>>, Integer, Hash)> list_job_applications_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_job_applications_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<JobApplication>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->list_job_applications_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posting_id** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**Array&lt;JobApplication&gt;**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_public_postings

> <Array<PublicPosting>> list_public_postings



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new

begin
  
  result = api_instance.list_public_postings
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->list_public_postings: #{e}"
end
```

#### Using the list_public_postings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PublicPosting>>, Integer, Hash)> list_public_postings_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_public_postings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PublicPosting>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->list_public_postings_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;PublicPosting&gt;**](PublicPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## score_job_application

> <JobApplication> score_job_application(application_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new
application_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.score_job_application(application_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->score_job_application: #{e}"
end
```

#### Using the score_job_application_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobApplication>, Integer, Hash)> score_job_application_with_http_info(application_id)

```ruby
begin
  
  data, status_code, headers = api_instance.score_job_application_with_http_info(application_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobApplication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->score_job_application_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **application_id** | **String** |  |  |

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_job_application_status

> <JobApplication> update_job_application_status(application_id, application_status_dto)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobApplicationApi.new
application_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
application_status_dto = SimplebillyApi::ApplicationStatusDto.new({status: 'status_example'}) # ApplicationStatusDto | 

begin
  
  result = api_instance.update_job_application_status(application_id, application_status_dto)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->update_job_application_status: #{e}"
end
```

#### Using the update_job_application_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobApplication>, Integer, Hash)> update_job_application_status_with_http_info(application_id, application_status_dto)

```ruby
begin
  
  data, status_code, headers = api_instance.update_job_application_status_with_http_info(application_id, application_status_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobApplication>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobApplicationApi->update_job_application_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **application_id** | **String** |  |  |
| **application_status_dto** | [**ApplicationStatusDto**](ApplicationStatusDto.md) |  |  |

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

