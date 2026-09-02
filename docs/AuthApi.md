# SimplebillyApi::AuthApi

All URIs are relative to *https://demo.simplebilly.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**accept_invite**](AuthApi.md#accept_invite) | **POST** /auth/accept-invite | Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox. |
| [**forgot_password**](AuthApi.md#forgot_password) | **POST** /auth/forgot-password | Send a password reset email to the user |
| [**login**](AuthApi.md#login) | **POST** /auth/login | Authenticate a user with email + password (optional TOTP) |
| [**logout**](AuthApi.md#logout) | **POST** /auth/logout | Log out the current user (kills the assay session) |
| [**magic_link_login**](AuthApi.md#magic_link_login) | **POST** /auth/magic-link | Request a magic link login (sends an email with a one-time link) |
| [**magic_link_verify**](AuthApi.md#magic_link_verify) | **POST** /auth/magic-link/verify | Verify a magic link token and log the user in |
| [**register**](AuthApi.md#register) | **POST** /auth/register | Register a new user account |
| [**reset_password**](AuthApi.md#reset_password) | **POST** /auth/reset-password | Reset the user&#39;s password using a reset token |
| [**totp_enable**](AuthApi.md#totp_enable) | **POST** /auth/totp/enable | Enable TOTP two-factor authentication by verifying a code |
| [**totp_setup**](AuthApi.md#totp_setup) | **GET** /auth/totp/setup | Set up TOTP two-factor authentication (generates secret + backup codes) |
| [**verify_email**](AuthApi.md#verify_email) | **POST** /auth/verify-email | Verify a user&#39;s email address using a verification token |


## accept_invite

> accept_invite(accept_invite_request)

Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
accept_invite_request = SimplebillyApi::AcceptInviteRequest.new({first_name: 'first_name_example', last_name: 'last_name_example', password: 'password_example', privacy_accepted: false, token: 'token_example'}) # AcceptInviteRequest | 

begin
  # Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
  api_instance.accept_invite(accept_invite_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->accept_invite: #{e}"
end
```

#### Using the accept_invite_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> accept_invite_with_http_info(accept_invite_request)

```ruby
begin
  # Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
  data, status_code, headers = api_instance.accept_invite_with_http_info(accept_invite_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->accept_invite_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **accept_invite_request** | [**AcceptInviteRequest**](AcceptInviteRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## forgot_password

> forgot_password(forgot_password_request)

Send a password reset email to the user

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
forgot_password_request = SimplebillyApi::ForgotPasswordRequest.new({email: 'email_example'}) # ForgotPasswordRequest | 

begin
  # Send a password reset email to the user
  api_instance.forgot_password(forgot_password_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->forgot_password: #{e}"
end
```

#### Using the forgot_password_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> forgot_password_with_http_info(forgot_password_request)

```ruby
begin
  # Send a password reset email to the user
  data, status_code, headers = api_instance.forgot_password_with_http_info(forgot_password_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->forgot_password_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **forgot_password_request** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## login

> <AuthResponse> login(login_request)

Authenticate a user with email + password (optional TOTP)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
login_request = SimplebillyApi::LoginRequest.new({email: 'email_example', password: 'password_example'}) # LoginRequest | 

begin
  # Authenticate a user with email + password (optional TOTP)
  result = api_instance.login(login_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->login: #{e}"
end
```

#### Using the login_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthResponse>, Integer, Hash)> login_with_http_info(login_request)

```ruby
begin
  # Authenticate a user with email + password (optional TOTP)
  data, status_code, headers = api_instance.login_with_http_info(login_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->login_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **login_request** | [**LoginRequest**](LoginRequest.md) |  |  |

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## logout

> logout

Log out the current user (kills the assay session)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new

begin
  # Log out the current user (kills the assay session)
  api_instance.logout
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->logout: #{e}"
end
```

#### Using the logout_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> logout_with_http_info

```ruby
begin
  # Log out the current user (kills the assay session)
  data, status_code, headers = api_instance.logout_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->logout_with_http_info: #{e}"
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


## magic_link_login

> magic_link_login(magic_link_request)

Request a magic link login (sends an email with a one-time link)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
magic_link_request = SimplebillyApi::MagicLinkRequest.new({email: 'email_example'}) # MagicLinkRequest | 

begin
  # Request a magic link login (sends an email with a one-time link)
  api_instance.magic_link_login(magic_link_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->magic_link_login: #{e}"
end
```

#### Using the magic_link_login_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> magic_link_login_with_http_info(magic_link_request)

```ruby
begin
  # Request a magic link login (sends an email with a one-time link)
  data, status_code, headers = api_instance.magic_link_login_with_http_info(magic_link_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->magic_link_login_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **magic_link_request** | [**MagicLinkRequest**](MagicLinkRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## magic_link_verify

> <AuthResponse> magic_link_verify(magic_link_verify_request)

Verify a magic link token and log the user in

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
magic_link_verify_request = SimplebillyApi::MagicLinkVerifyRequest.new({token: 'token_example'}) # MagicLinkVerifyRequest | 

begin
  # Verify a magic link token and log the user in
  result = api_instance.magic_link_verify(magic_link_verify_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->magic_link_verify: #{e}"
end
```

#### Using the magic_link_verify_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthResponse>, Integer, Hash)> magic_link_verify_with_http_info(magic_link_verify_request)

```ruby
begin
  # Verify a magic link token and log the user in
  data, status_code, headers = api_instance.magic_link_verify_with_http_info(magic_link_verify_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->magic_link_verify_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **magic_link_verify_request** | [**MagicLinkVerifyRequest**](MagicLinkVerifyRequest.md) |  |  |

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## register

> <AuthResponse> register(register_request)

Register a new user account

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
register_request = SimplebillyApi::RegisterRequest.new({company_name: 'company_name_example', email: 'email_example', first_name: 'first_name_example', last_name: 'last_name_example', password: 'password_example', privacy_accepted: false}) # RegisterRequest | 

begin
  # Register a new user account
  result = api_instance.register(register_request)
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->register: #{e}"
end
```

#### Using the register_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthResponse>, Integer, Hash)> register_with_http_info(register_request)

```ruby
begin
  # Register a new user account
  data, status_code, headers = api_instance.register_with_http_info(register_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->register_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **register_request** | [**RegisterRequest**](RegisterRequest.md) |  |  |

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## reset_password

> reset_password(reset_password_request)

Reset the user's password using a reset token

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
reset_password_request = SimplebillyApi::ResetPasswordRequest.new({new_password: 'new_password_example', token: 'token_example'}) # ResetPasswordRequest | 

begin
  # Reset the user's password using a reset token
  api_instance.reset_password(reset_password_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->reset_password: #{e}"
end
```

#### Using the reset_password_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> reset_password_with_http_info(reset_password_request)

```ruby
begin
  # Reset the user's password using a reset token
  data, status_code, headers = api_instance.reset_password_with_http_info(reset_password_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->reset_password_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reset_password_request** | [**ResetPasswordRequest**](ResetPasswordRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## totp_enable

> totp_enable(totp_enable_request)

Enable TOTP two-factor authentication by verifying a code

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
totp_enable_request = SimplebillyApi::TotpEnableRequest.new({code: 'code_example'}) # TotpEnableRequest | 

begin
  # Enable TOTP two-factor authentication by verifying a code
  api_instance.totp_enable(totp_enable_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->totp_enable: #{e}"
end
```

#### Using the totp_enable_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> totp_enable_with_http_info(totp_enable_request)

```ruby
begin
  # Enable TOTP two-factor authentication by verifying a code
  data, status_code, headers = api_instance.totp_enable_with_http_info(totp_enable_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->totp_enable_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **totp_enable_request** | [**TotpEnableRequest**](TotpEnableRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## totp_setup

> <TotpSetupResponse> totp_setup

Set up TOTP two-factor authentication (generates secret + backup codes)

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new

begin
  # Set up TOTP two-factor authentication (generates secret + backup codes)
  result = api_instance.totp_setup
  p result
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->totp_setup: #{e}"
end
```

#### Using the totp_setup_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TotpSetupResponse>, Integer, Hash)> totp_setup_with_http_info

```ruby
begin
  # Set up TOTP two-factor authentication (generates secret + backup codes)
  data, status_code, headers = api_instance.totp_setup_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TotpSetupResponse>
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->totp_setup_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**TotpSetupResponse**](TotpSetupResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## verify_email

> verify_email(verify_email_request)

Verify a user's email address using a verification token

### Examples

```ruby
require 'time'
require 'simplebilly_api'
# setup authorization
SimplebillyApi.configure do |config|
  # Configure Bearer authorization (JWT): bearer_token
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = SimplebillyApi::AuthApi.new
verify_email_request = SimplebillyApi::VerifyEmailRequest.new({token: 'token_example'}) # VerifyEmailRequest | 

begin
  # Verify a user's email address using a verification token
  api_instance.verify_email(verify_email_request)
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->verify_email: #{e}"
end
```

#### Using the verify_email_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> verify_email_with_http_info(verify_email_request)

```ruby
begin
  # Verify a user's email address using a verification token
  data, status_code, headers = api_instance.verify_email_with_http_info(verify_email_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue SimplebillyApi::ApiError => e
  puts "Error when calling AuthApi->verify_email_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **verify_email_request** | [**VerifyEmailRequest**](VerifyEmailRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

