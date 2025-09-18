# IdpluggerPromotion\AuthApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**authLoginByToken()**](AuthApi.md#authLoginByToken) | **POST** /v3/auth/login | Login na API via e-mail e token |
| [**authRefreshToken()**](AuthApi.md#authRefreshToken) | **POST** /v3/auth/refresh | Renova o do token de autenticação |
| [**authRequestToken()**](AuthApi.md#authRequestToken) | **POST** /v3/auth/request-token | Solicita envio de token de login por email |
| [**login()**](AuthApi.md#login) | **POST** /v3/login | Login na API |
| [**me()**](AuthApi.md#me) | **GET** /v3/me | Dados na API |


## `authLoginByToken()`

```php
authLoginByToken($auth_login_by_token_request): \IdpluggerPromotion\Model\AuthLoginByToken200Response
```

Login na API via e-mail e token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new IdpluggerPromotion\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_login_by_token_request = new \IdpluggerPromotion\Model\AuthLoginByTokenRequest(); // \IdpluggerPromotion\Model\AuthLoginByTokenRequest

try {
    $result = $apiInstance->authLoginByToken($auth_login_by_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->authLoginByToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_login_by_token_request** | [**\IdpluggerPromotion\Model\AuthLoginByTokenRequest**](../Model/AuthLoginByTokenRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\AuthLoginByToken200Response**](../Model/AuthLoginByToken200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authRefreshToken()`

```php
authRefreshToken($auth_refresh_token_request): \IdpluggerPromotion\Model\AuthLoginByToken200Response
```

Renova o do token de autenticação

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new IdpluggerPromotion\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_refresh_token_request = new \IdpluggerPromotion\Model\AuthRefreshTokenRequest(); // \IdpluggerPromotion\Model\AuthRefreshTokenRequest

try {
    $result = $apiInstance->authRefreshToken($auth_refresh_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->authRefreshToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_refresh_token_request** | [**\IdpluggerPromotion\Model\AuthRefreshTokenRequest**](../Model/AuthRefreshTokenRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\AuthLoginByToken200Response**](../Model/AuthLoginByToken200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `authRequestToken()`

```php
authRequestToken($auth_request_token_request): \IdpluggerPromotion\Model\AuthRequestToken200Response
```

Solicita envio de token de login por email

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new IdpluggerPromotion\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_request_token_request = new \IdpluggerPromotion\Model\AuthRequestTokenRequest(); // \IdpluggerPromotion\Model\AuthRequestTokenRequest

try {
    $result = $apiInstance->authRequestToken($auth_request_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->authRequestToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_request_token_request** | [**\IdpluggerPromotion\Model\AuthRequestTokenRequest**](../Model/AuthRequestTokenRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\AuthRequestToken200Response**](../Model/AuthRequestToken200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `login()`

```php
login($login_request): \IdpluggerPromotion\Model\Login200Response
```

Login na API

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new IdpluggerPromotion\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$login_request = new \IdpluggerPromotion\Model\LoginRequest(); // \IdpluggerPromotion\Model\LoginRequest

try {
    $result = $apiInstance->login($login_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->login: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **login_request** | [**\IdpluggerPromotion\Model\LoginRequest**](../Model/LoginRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\Login200Response**](../Model/Login200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `me()`

```php
me(): \IdpluggerPromotion\Model\Me200Response
```

Dados na API

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->me();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->me: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\IdpluggerPromotion\Model\Me200Response**](../Model/Me200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
