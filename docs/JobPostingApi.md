# SimplebillyApi::JobPostingApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_job_posting**](JobPostingApi.md#create_job_posting) | **POST** /api/v1/job-postings |  |
| [**delete_job_posting**](JobPostingApi.md#delete_job_posting) | **DELETE** /api/v1/job-postings/{id} |  |
| [**get_job_posting**](JobPostingApi.md#get_job_posting) | **GET** /api/v1/job-postings/{id} |  |
| [**list_job_postings**](JobPostingApi.md#list_job_postings) | **GET** /api/v1/job-postings |  |
| [**update_job_posting**](JobPostingApi.md#update_job_posting) | **PUT** /api/v1/job-postings/{id} |  |


## create_job_posting

> <JobPosting> create_job_posting(job_posting_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobPostingApi.new
job_posting_create = SimplebillyApi::JobPostingCreate.new({description: 'description_example', remote: false, required_skills: 3.56, status: SimplebillyApi::JobPostingStatus::DRAFT, title: 'title_example'}) # JobPostingCreate | 

begin
  
  result = api_instance.create_job_posting(job_posting_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->create_job_posting: #{e}"
end
```

#### Using the create_job_posting_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobPosting>, Integer, Hash)> create_job_posting_with_http_info(job_posting_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_job_posting_with_http_info(job_posting_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobPosting>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->create_job_posting_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_posting_create** | [**JobPostingCreate**](JobPostingCreate.md) |  |  |

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_job_posting

> delete_job_posting(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobPostingApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  api_instance.delete_job_posting(id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->delete_job_posting: #{e}"
end
```

#### Using the delete_job_posting_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_job_posting_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_job_posting_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->delete_job_posting_with_http_info: #{e}"
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


## get_job_posting

> <JobPosting> get_job_posting(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobPostingApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.get_job_posting(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->get_job_posting: #{e}"
end
```

#### Using the get_job_posting_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobPosting>, Integer, Hash)> get_job_posting_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.get_job_posting_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobPosting>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->get_job_posting_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_job_postings

> <Array<JobPosting>> list_job_postings(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobPostingApi.new
opts = {
  status: 'status_example', # String | 
  page: 56, # Integer | 
  page_size: 56 # Integer | 
}

begin
  
  result = api_instance.list_job_postings(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->list_job_postings: #{e}"
end
```

#### Using the list_job_postings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<JobPosting>>, Integer, Hash)> list_job_postings_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.list_job_postings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<JobPosting>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->list_job_postings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **page** | **Integer** |  | [optional] |
| **page_size** | **Integer** |  | [optional] |

### Return type

[**Array&lt;JobPosting&gt;**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_job_posting

> <JobPosting> update_job_posting(id, job_posting_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::JobPostingApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
job_posting_update = SimplebillyApi::JobPostingUpdate.new # JobPostingUpdate | 

begin
  
  result = api_instance.update_job_posting(id, job_posting_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->update_job_posting: #{e}"
end
```

#### Using the update_job_posting_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobPosting>, Integer, Hash)> update_job_posting_with_http_info(id, job_posting_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_job_posting_with_http_info(id, job_posting_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobPosting>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling JobPostingApi->update_job_posting_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **job_posting_update** | [**JobPostingUpdate**](JobPostingUpdate.md) |  |  |

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

