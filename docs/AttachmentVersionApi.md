# SimplebillyApi::AttachmentVersionApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_attachment_version**](AttachmentVersionApi.md#create_attachment_version) | **POST** /api/v1/attachments/{attachment_id}/versions |  |
| [**list_attachment_versions**](AttachmentVersionApi.md#list_attachment_versions) | **GET** /api/v1/attachments/{attachment_id}/versions |  |
| [**restore_attachment_version**](AttachmentVersionApi.md#restore_attachment_version) | **POST** /api/v1/attachments/{attachment_id}/versions/{version_id}/restore |  |


## create_attachment_version

> <AttachmentVersion> create_attachment_version(attachment_id, new_version_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentVersionApi.new
attachment_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
new_version_request = SimplebillyApi::NewVersionRequest.new({file_name: 'file_name_example'}) # NewVersionRequest | 

begin
  
  result = api_instance.create_attachment_version(attachment_id, new_version_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentVersionApi->create_attachment_version: #{e}"
end
```

#### Using the create_attachment_version_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AttachmentVersion>, Integer, Hash)> create_attachment_version_with_http_info(attachment_id, new_version_request)

```ruby
begin
  
  data, status_code, headers = api_instance.create_attachment_version_with_http_info(attachment_id, new_version_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AttachmentVersion>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentVersionApi->create_attachment_version_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attachment_id** | **String** |  |  |
| **new_version_request** | [**NewVersionRequest**](NewVersionRequest.md) |  |  |

### Return type

[**AttachmentVersion**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_attachment_versions

> <Array<AttachmentVersion>> list_attachment_versions(attachment_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentVersionApi.new
attachment_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.list_attachment_versions(attachment_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentVersionApi->list_attachment_versions: #{e}"
end
```

#### Using the list_attachment_versions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AttachmentVersion>>, Integer, Hash)> list_attachment_versions_with_http_info(attachment_id)

```ruby
begin
  
  data, status_code, headers = api_instance.list_attachment_versions_with_http_info(attachment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AttachmentVersion>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentVersionApi->list_attachment_versions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attachment_id** | **String** |  |  |

### Return type

[**Array&lt;AttachmentVersion&gt;**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## restore_attachment_version

> <Attachment> restore_attachment_version(attachment_id, version_id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AttachmentVersionApi.new
attachment_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
version_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.restore_attachment_version(attachment_id, version_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentVersionApi->restore_attachment_version: #{e}"
end
```

#### Using the restore_attachment_version_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Attachment>, Integer, Hash)> restore_attachment_version_with_http_info(attachment_id, version_id)

```ruby
begin
  
  data, status_code, headers = api_instance.restore_attachment_version_with_http_info(attachment_id, version_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Attachment>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AttachmentVersionApi->restore_attachment_version_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attachment_id** | **String** |  |  |
| **version_id** | **String** |  |  |

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

