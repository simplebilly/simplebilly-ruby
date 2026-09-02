# SimplebillyApi::PostingCategoryApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_posting_category**](PostingCategoryApi.md#create_posting_category) | **POST** /api/v1/posting-categories |  |
| [**delete_posting_category**](PostingCategoryApi.md#delete_posting_category) | **DELETE** /api/v1/posting-categories/{category_id} |  |
| [**list_posting_categories**](PostingCategoryApi.md#list_posting_categories) | **GET** /api/v1/posting-categories |  |
| [**seed_posting_categories**](PostingCategoryApi.md#seed_posting_categories) | **POST** /api/v1/posting-categories/seed/{skr_version} |  |
| [**update_posting_category**](PostingCategoryApi.md#update_posting_category) | **PUT** /api/v1/posting-categories/{category_id} |  |


## create_posting_category

> <PostingCategory> create_posting_category(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PostingCategoryApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.create_posting_category(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->create_posting_category: #{e}"
end
```

#### Using the create_posting_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostingCategory>, Integer, Hash)> create_posting_category_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.create_posting_category_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostingCategory>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->create_posting_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

[**PostingCategory**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_posting_category

> delete_posting_category(category_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PostingCategoryApi.new
category_id = 'category_id_example' # String | 

begin
  
  api_instance.delete_posting_category(category_id)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->delete_posting_category: #{e}"
end
```

#### Using the delete_posting_category_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_posting_category_with_http_info(category_id)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_posting_category_with_http_info(category_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->delete_posting_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_posting_categories

> <Array<PostingCategory>> list_posting_categories



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PostingCategoryApi.new

begin
  
  result = api_instance.list_posting_categories
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->list_posting_categories: #{e}"
end
```

#### Using the list_posting_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PostingCategory>>, Integer, Hash)> list_posting_categories_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.list_posting_categories_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PostingCategory>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->list_posting_categories_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;PostingCategory&gt;**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## seed_posting_categories

> seed_posting_categories(skr_version)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PostingCategoryApi.new
skr_version = 'skr_version_example' # String | 

begin
  
  api_instance.seed_posting_categories(skr_version)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->seed_posting_categories: #{e}"
end
```

#### Using the seed_posting_categories_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> seed_posting_categories_with_http_info(skr_version)

```ruby
begin
  
  data, status_code, headers = api_instance.seed_posting_categories_with_http_info(skr_version)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->seed_posting_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **skr_version** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_posting_category

> <PostingCategory> update_posting_category(category_id, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PostingCategoryApi.new
category_id = 'category_id_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.update_posting_category(category_id, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->update_posting_category: #{e}"
end
```

#### Using the update_posting_category_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostingCategory>, Integer, Hash)> update_posting_category_with_http_info(category_id, body)

```ruby
begin
  
  data, status_code, headers = api_instance.update_posting_category_with_http_info(category_id, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostingCategory>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PostingCategoryApi->update_posting_category_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

[**PostingCategory**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

