# SimplebillyApi::GroupFigureApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_group_figure**](GroupFigureApi.md#create_group_figure) | **POST** /api/v1/group-figures |  |
| [**delete_group_figure**](GroupFigureApi.md#delete_group_figure) | **DELETE** /api/v1/group-figures/{year} |  |
| [**get_group_figure**](GroupFigureApi.md#get_group_figure) | **GET** /api/v1/group-figures/{year} |  |
| [**get_group_figures**](GroupFigureApi.md#get_group_figures) | **GET** /api/v1/group-figures/ |  |
| [**update_group_figure**](GroupFigureApi.md#update_group_figure) | **PUT** /api/v1/group-figures/{year} |  |


## create_group_figure

> <GroupFigure> create_group_figure(group_figure_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GroupFigureApi.new
group_figure_create = SimplebillyApi::GroupFigureCreate.new # GroupFigureCreate | 

begin
  
  result = api_instance.create_group_figure(group_figure_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->create_group_figure: #{e}"
end
```

#### Using the create_group_figure_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GroupFigure>, Integer, Hash)> create_group_figure_with_http_info(group_figure_create)

```ruby
begin
  
  data, status_code, headers = api_instance.create_group_figure_with_http_info(group_figure_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GroupFigure>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->create_group_figure_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **group_figure_create** | [**GroupFigureCreate**](GroupFigureCreate.md) |  |  |

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_group_figure

> delete_group_figure(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GroupFigureApi.new
year = 56 # Integer | 

begin
  
  api_instance.delete_group_figure(year)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->delete_group_figure: #{e}"
end
```

#### Using the delete_group_figure_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_group_figure_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.delete_group_figure_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->delete_group_figure_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_group_figure

> <GroupFigure> get_group_figure(year)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GroupFigureApi.new
year = 56 # Integer | 

begin
  
  result = api_instance.get_group_figure(year)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->get_group_figure: #{e}"
end
```

#### Using the get_group_figure_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GroupFigure>, Integer, Hash)> get_group_figure_with_http_info(year)

```ruby
begin
  
  data, status_code, headers = api_instance.get_group_figure_with_http_info(year)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GroupFigure>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->get_group_figure_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_group_figures

> <Array<GroupFigure>> get_group_figures(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GroupFigureApi.new
opts = {
  page: 1, # Integer | 
  page_size: 56, # Integer | 
  search: 'search_example', # String | 
  include_deleted: true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
}

begin
  
  result = api_instance.get_group_figures(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->get_group_figures: #{e}"
end
```

#### Using the get_group_figures_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<GroupFigure>>, Integer, Hash)> get_group_figures_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.get_group_figures_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<GroupFigure>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->get_group_figures_with_http_info: #{e}"
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

[**Array&lt;GroupFigure&gt;**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_group_figure

> <GroupFigure> update_group_figure(year, group_figure_update)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GroupFigureApi.new
year = 56 # Integer | 
group_figure_update = SimplebillyApi::GroupFigureUpdate.new # GroupFigureUpdate | 

begin
  
  result = api_instance.update_group_figure(year, group_figure_update)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->update_group_figure: #{e}"
end
```

#### Using the update_group_figure_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GroupFigure>, Integer, Hash)> update_group_figure_with_http_info(year, group_figure_update)

```ruby
begin
  
  data, status_code, headers = api_instance.update_group_figure_with_http_info(year, group_figure_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GroupFigure>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GroupFigureApi->update_group_figure_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |
| **group_figure_update** | [**GroupFigureUpdate**](GroupFigureUpdate.md) |  |  |

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

