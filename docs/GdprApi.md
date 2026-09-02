# SimplebillyApi::GdprApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**accept_dpa**](GdprApi.md#accept_dpa) | **PUT** /api/v1/gdpr/dpa | Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing). |
| [**account_erasure**](GdprApi.md#account_erasure) | **POST** /api/v1/gdpr/account-erasure | Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination). |
| [**erasure_contact**](GdprApi.md#erasure_contact) | **POST** /api/v1/gdpr/erasure/{contact_id} | Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on &#x60;contacts&#x60; already records who/when. |
| [**export_contact_data**](GdprApi.md#export_contact_data) | **GET** /api/v1/gdpr/export/{contact_id} | Art. 15 data-subject access export for a contact. |
| [**export_gdpr**](GdprApi.md#export_gdpr) | **GET** /api/v1/gdpr/export | Export the current user&#39;s personal data (GDPR Art. 15/20). |
| [**get_dpa**](GdprApi.md#get_dpa) | **GET** /api/v1/gdpr/dpa | Current DPA acceptance status (from tenant_settings). |


## accept_dpa

> <DpaStatus> accept_dpa(dpa_accept_request)

Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GdprApi.new
dpa_accept_request = SimplebillyApi::DpaAcceptRequest.new({accepted_by_name: 'accepted_by_name_example', version: 'version_example'}) # DpaAcceptRequest | 

begin
  # Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
  result = api_instance.accept_dpa(dpa_accept_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->accept_dpa: #{e}"
end
```

#### Using the accept_dpa_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DpaStatus>, Integer, Hash)> accept_dpa_with_http_info(dpa_accept_request)

```ruby
begin
  # Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
  data, status_code, headers = api_instance.accept_dpa_with_http_info(dpa_accept_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DpaStatus>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->accept_dpa_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **dpa_accept_request** | [**DpaAcceptRequest**](DpaAcceptRequest.md) |  |  |

### Return type

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## account_erasure

> Object account_erasure

Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).

Anonymizes every contact, anonymizes personal fields on bookkeeping records (orders/invoices/payments keep amounts and dates for GoBD), removes the tenant linkage of the (global, saasy-framework) users and marks the erasure on `tenant_settings.gdpr_erased_at`. No row is physically deleted. The audit triggers on the touched tables record who/when.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GdprApi.new

begin
  # Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
  result = api_instance.account_erasure
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->account_erasure: #{e}"
end
```

#### Using the account_erasure_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> account_erasure_with_http_info

```ruby
begin
  # Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
  data, status_code, headers = api_instance.account_erasure_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->account_erasure_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## erasure_contact

> Object erasure_contact(contact_id)

Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GdprApi.new
contact_id = 'contact_id_example' # String | 

begin
  # Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.
  result = api_instance.erasure_contact(contact_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->erasure_contact: #{e}"
end
```

#### Using the erasure_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> erasure_contact_with_http_info(contact_id)

```ruby
begin
  # Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.
  data, status_code, headers = api_instance.erasure_contact_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->erasure_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## export_contact_data

> Object export_contact_data(contact_id)

Art. 15 data-subject access export for a contact.

Returns the contact itself plus the tenant-scoped rows linked to it.  ## Relations The `customers`/`orders`/`invoices`/`payments` tables have no FK to `contacts`; they are linked through the `customer_id` column, which per the app's conventions holds one of: - the admin customer's `customer_id` (a UUID, often the same value as   the contact's `contact_id`/`customer_number`), - the buyer's email for shop orders, or - the marketplace's external customer id for plugin orders.  The export therefore matches the contact's identifiers (`contact_id`, `customer_number`, `external_id`, `email`) plus any resolved customer ids against `customer_id`. `delivery_notes` and `customer_communications` reference contacts directly via `contact_id`. Soft-deleted rows are included (their data is still processed and retained for GoBD). Relations that genuinely do not exist for a contact stay empty but the key is always present.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GdprApi.new
contact_id = 'contact_id_example' # String | 

begin
  # Art. 15 data-subject access export for a contact.
  result = api_instance.export_contact_data(contact_id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->export_contact_data: #{e}"
end
```

#### Using the export_contact_data_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> export_contact_data_with_http_info(contact_id)

```ruby
begin
  # Art. 15 data-subject access export for a contact.
  data, status_code, headers = api_instance.export_contact_data_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->export_contact_data_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## export_gdpr

> <ApiResponseGdprExport> export_gdpr

Export the current user's personal data (GDPR Art. 15/20).

No admin permission required: a user always exports their own data.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GdprApi.new

begin
  # Export the current user's personal data (GDPR Art. 15/20).
  result = api_instance.export_gdpr
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->export_gdpr: #{e}"
end
```

#### Using the export_gdpr_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiResponseGdprExport>, Integer, Hash)> export_gdpr_with_http_info

```ruby
begin
  # Export the current user's personal data (GDPR Art. 15/20).
  data, status_code, headers = api_instance.export_gdpr_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiResponseGdprExport>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->export_gdpr_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiResponseGdprExport**](ApiResponseGdprExport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_dpa

> <DpaStatus> get_dpa

Current DPA acceptance status (from tenant_settings).

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::GdprApi.new

begin
  # Current DPA acceptance status (from tenant_settings).
  result = api_instance.get_dpa
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->get_dpa: #{e}"
end
```

#### Using the get_dpa_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DpaStatus>, Integer, Hash)> get_dpa_with_http_info

```ruby
begin
  # Current DPA acceptance status (from tenant_settings).
  data, status_code, headers = api_instance.get_dpa_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DpaStatus>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling GdprApi->get_dpa_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

