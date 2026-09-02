# SimplebillyApi::BudgetsApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**budgets_api**](BudgetsApi.md#budgets_api) | **GET** /api/v1/bookkeeping/budgets |  |
| [**upsert_budget_goal_api**](BudgetsApi.md#upsert_budget_goal_api) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} |  |


## budgets_api

> <BudgetErgebnis> budgets_api(year, month)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BudgetsApi.new
year = 56 # Integer | 
month = 56 # Integer | 

begin
  
  result = api_instance.budgets_api(year, month)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BudgetsApi->budgets_api: #{e}"
end
```

#### Using the budgets_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BudgetErgebnis>, Integer, Hash)> budgets_api_with_http_info(year, month)

```ruby
begin
  
  data, status_code, headers = api_instance.budgets_api_with_http_info(year, month)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BudgetErgebnis>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BudgetsApi->budgets_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** |  |  |
| **month** | **Integer** |  |  |

### Return type

[**BudgetErgebnis**](BudgetErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## upsert_budget_goal_api

> <Budget> upsert_budget_goal_api(category, budget_goal_request)



### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::BudgetsApi.new
category = 'category_example' # String | 
budget_goal_request = SimplebillyApi::BudgetGoalRequest.new({monthly_goal: 'monthly_goal_example', year: 37}) # BudgetGoalRequest | 

begin
  
  result = api_instance.upsert_budget_goal_api(category, budget_goal_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BudgetsApi->upsert_budget_goal_api: #{e}"
end
```

#### Using the upsert_budget_goal_api_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Budget>, Integer, Hash)> upsert_budget_goal_api_with_http_info(category, budget_goal_request)

```ruby
begin
  
  data, status_code, headers = api_instance.upsert_budget_goal_api_with_http_info(category, budget_goal_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Budget>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling BudgetsApi->upsert_budget_goal_api_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category** | **String** |  |  |
| **budget_goal_request** | [**BudgetGoalRequest**](BudgetGoalRequest.md) |  |  |

### Return type

[**Budget**](Budget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

