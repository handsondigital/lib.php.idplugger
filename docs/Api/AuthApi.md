# IdpluggerPromotion\AuthApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**login()**](AuthApi.md#login) | **POST** /v3/login | Login na API |
| [**me()**](AuthApi.md#me) | **GET** /v3/me | Dados na API |


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
