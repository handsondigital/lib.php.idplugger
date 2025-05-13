# IdPluggerPromotion\AutenticaoApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**appHttpControllersAdminAdminControllerLogin()**](AutenticaoApi.md#appHttpControllersAdminAdminControllerLogin) | **POST** /v3/login | Login na API |
| [**appHttpControllersAdminAdminControllerMe()**](AutenticaoApi.md#appHttpControllersAdminAdminControllerMe) | **GET** /v3/me | Dados na API |


## `appHttpControllersAdminAdminControllerLogin()`

```php
appHttpControllersAdminAdminControllerLogin($app_http_controllers_admin_admin_controller_login_request): \IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerLogin200Response
```

Login na API

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new IdPluggerPromotion\Api\AutenticaoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$app_http_controllers_admin_admin_controller_login_request = new \IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerLoginRequest(); // \IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerLoginRequest

try {
    $result = $apiInstance->appHttpControllersAdminAdminControllerLogin($app_http_controllers_admin_admin_controller_login_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutenticaoApi->appHttpControllersAdminAdminControllerLogin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_http_controllers_admin_admin_controller_login_request** | [**\IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerLoginRequest**](../Model/AppHttpControllersAdminAdminControllerLoginRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerLogin200Response**](../Model/AppHttpControllersAdminAdminControllerLogin200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appHttpControllersAdminAdminControllerMe()`

```php
appHttpControllersAdminAdminControllerMe(): \IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerMe200Response
```

Dados na API

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\AutenticaoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->appHttpControllersAdminAdminControllerMe();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutenticaoApi->appHttpControllersAdminAdminControllerMe: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\IdPluggerPromotion\Model\AppHttpControllersAdminAdminControllerMe200Response**](../Model/AppHttpControllersAdminAdminControllerMe200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
