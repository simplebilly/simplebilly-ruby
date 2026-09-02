# SimplebillyApi::PosApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**pos_billing**](PosApi.md#pos_billing) | **GET** /api/pos/billing |  |
| [**pos_create_order**](PosApi.md#pos_create_order) | **POST** /api/pos/orders |  |
| [**pos_create_register**](PosApi.md#pos_create_register) | **POST** /api/pos/registers |  |
| [**pos_create_table**](PosApi.md#pos_create_table) | **POST** /api/pos/tables |  |
| [**pos_disable_register**](PosApi.md#pos_disable_register) | **POST** /api/pos/registers/{id}/disable |  |
| [**pos_free_table**](PosApi.md#pos_free_table) | **POST** /api/pos/tables/{id}/free |  |
| [**pos_kasse_closing**](PosApi.md#pos_kasse_closing) | **POST** /api/pos/kasse/closing |  |
| [**pos_kasse_entries**](PosApi.md#pos_kasse_entries) | **GET** /api/pos/kasse/entries |  |
| [**pos_kasse_export**](PosApi.md#pos_kasse_export) | **GET** /api/pos/kasse/export |  |
| [**pos_kasse_pay_in_out**](PosApi.md#pos_kasse_pay_in_out) | **POST** /api/pos/kasse/pay-in-out |  |
| [**pos_list_orders**](PosApi.md#pos_list_orders) | **GET** /api/pos/orders |  |
| [**pos_list_products**](PosApi.md#pos_list_products) | **GET** /api/pos/products |  |
| [**pos_list_registers**](PosApi.md#pos_list_registers) | **GET** /api/pos/registers |  |
| [**pos_list_tables**](PosApi.md#pos_list_tables) | **GET** /api/pos/tables |  |
| [**pos_order_print**](PosApi.md#pos_order_print) | **GET** /api/pos/orders/{order_number}/print |  |
| [**pos_order_receipt**](PosApi.md#pos_order_receipt) | **GET** /api/pos/orders/{order_number}/receipt |  |
| [**pos_pay_order**](PosApi.md#pos_pay_order) | **POST** /api/pos/orders/{order_number}/pay |  |
| [**pos_sumup_checkout**](PosApi.md#pos_sumup_checkout) | **POST** /api/pos/sumup/checkout |  |


## pos_billing

> Object pos_billing



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new

begin
  
  result = api_instance.pos_billing
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_billing: #{e}"
end
```

#### Using the pos_billing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_billing_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.pos_billing_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_billing_with_http_info: #{e}"
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


## pos_create_order

> Object pos_create_order(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.pos_create_order(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_create_order: #{e}"
end
```

#### Using the pos_create_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_create_order_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_create_order_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_create_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pos_create_register

> <PosRegister> pos_create_register(pos_register_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
pos_register_create = SimplebillyApi::PosRegisterCreate.new({name: 'name_example'}) # PosRegisterCreate | 

begin
  
  result = api_instance.pos_create_register(pos_register_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_create_register: #{e}"
end
```

#### Using the pos_create_register_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PosRegister>, Integer, Hash)> pos_create_register_with_http_info(pos_register_create)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_create_register_with_http_info(pos_register_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PosRegister>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_create_register_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pos_register_create** | [**PosRegisterCreate**](PosRegisterCreate.md) |  |  |

### Return type

[**PosRegister**](PosRegister.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pos_create_table

> <PosTable> pos_create_table(pos_table_create)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
pos_table_create = SimplebillyApi::PosTableCreate.new({name: 'name_example'}) # PosTableCreate | 

begin
  
  result = api_instance.pos_create_table(pos_table_create)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_create_table: #{e}"
end
```

#### Using the pos_create_table_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PosTable>, Integer, Hash)> pos_create_table_with_http_info(pos_table_create)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_create_table_with_http_info(pos_table_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PosTable>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_create_table_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pos_table_create** | [**PosTableCreate**](PosTableCreate.md) |  |  |

### Return type

[**PosTable**](PosTable.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pos_disable_register

> <PosRegister> pos_disable_register(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.pos_disable_register(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_disable_register: #{e}"
end
```

#### Using the pos_disable_register_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PosRegister>, Integer, Hash)> pos_disable_register_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_disable_register_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PosRegister>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_disable_register_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**PosRegister**](PosRegister.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_free_table

> <PosTable> pos_free_table(id)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  
  result = api_instance.pos_free_table(id)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_free_table: #{e}"
end
```

#### Using the pos_free_table_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PosTable>, Integer, Hash)> pos_free_table_with_http_info(id)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_free_table_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PosTable>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_free_table_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |

### Return type

[**PosTable**](PosTable.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_kasse_closing

> Object pos_kasse_closing(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.pos_kasse_closing(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_closing: #{e}"
end
```

#### Using the pos_kasse_closing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_kasse_closing_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_kasse_closing_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_closing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pos_kasse_entries

> Object pos_kasse_entries



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new

begin
  
  result = api_instance.pos_kasse_entries
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_entries: #{e}"
end
```

#### Using the pos_kasse_entries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_kasse_entries_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.pos_kasse_entries_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_entries_with_http_info: #{e}"
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


## pos_kasse_export

> Object pos_kasse_export



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new

begin
  
  result = api_instance.pos_kasse_export
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_export: #{e}"
end
```

#### Using the pos_kasse_export_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_kasse_export_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.pos_kasse_export_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_export_with_http_info: #{e}"
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


## pos_kasse_pay_in_out

> Object pos_kasse_pay_in_out(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.pos_kasse_pay_in_out(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_pay_in_out: #{e}"
end
```

#### Using the pos_kasse_pay_in_out_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_kasse_pay_in_out_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_kasse_pay_in_out_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_kasse_pay_in_out_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pos_list_orders

> Object pos_list_orders(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
opts = {
  status: 'status_example' # String | Filter by order status
}

begin
  
  result = api_instance.pos_list_orders(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_orders: #{e}"
end
```

#### Using the pos_list_orders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_list_orders_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_list_orders_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_orders_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Filter by order status | [optional] |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_list_products

> Object pos_list_products(opts)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
opts = {
  q: 'q_example' # String | Product search
}

begin
  
  result = api_instance.pos_list_products(opts)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_products: #{e}"
end
```

#### Using the pos_list_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_list_products_with_http_info(opts)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_list_products_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Product search | [optional] |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_list_registers

> <Array<PosRegister>> pos_list_registers



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new

begin
  
  result = api_instance.pos_list_registers
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_registers: #{e}"
end
```

#### Using the pos_list_registers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PosRegister>>, Integer, Hash)> pos_list_registers_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.pos_list_registers_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PosRegister>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_registers_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;PosRegister&gt;**](PosRegister.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_list_tables

> <Array<PosTable>> pos_list_tables



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new

begin
  
  result = api_instance.pos_list_tables
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_tables: #{e}"
end
```

#### Using the pos_list_tables_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PosTable>>, Integer, Hash)> pos_list_tables_with_http_info

```ruby
begin
  
  data, status_code, headers = api_instance.pos_list_tables_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PosTable>>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_list_tables_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;PosTable&gt;**](PosTable.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_order_print

> Object pos_order_print(order_number)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
order_number = 'order_number_example' # String | 

begin
  
  result = api_instance.pos_order_print(order_number)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_order_print: #{e}"
end
```

#### Using the pos_order_print_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_order_print_with_http_info(order_number)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_order_print_with_http_info(order_number)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_order_print_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_order_receipt

> Object pos_order_receipt(order_number)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
order_number = 'order_number_example' # String | 

begin
  
  result = api_instance.pos_order_receipt(order_number)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_order_receipt: #{e}"
end
```

#### Using the pos_order_receipt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_order_receipt_with_http_info(order_number)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_order_receipt_with_http_info(order_number)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_order_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pos_pay_order

> Object pos_pay_order(order_number, body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
order_number = 'order_number_example' # String | 
body = 3.56 # Object | 

begin
  
  result = api_instance.pos_pay_order(order_number, body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_pay_order: #{e}"
end
```

#### Using the pos_pay_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_pay_order_with_http_info(order_number, body)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_pay_order_with_http_info(order_number, body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_pay_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** |  |  |
| **body** | **Object** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pos_sumup_checkout

> Object pos_sumup_checkout(body)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::PosApi.new
body = 3.56 # Object | 

begin
  
  result = api_instance.pos_sumup_checkout(body)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_sumup_checkout: #{e}"
end
```

#### Using the pos_sumup_checkout_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> pos_sumup_checkout_with_http_info(body)

```ruby
begin
  
  data, status_code, headers = api_instance.pos_sumup_checkout_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue SimplebillyApi::ApiError => e
  puts "Error when calling PosApi->pos_sumup_checkout_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **Object** |  |  |

### Return type

**Object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

