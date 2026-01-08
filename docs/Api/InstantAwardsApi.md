# IdpluggerPromotion\InstantAwardsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**instantAwardAttempts()**](InstantAwardsApi.md#instantAwardAttempts) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/attempts | Retorna a quantidade de chances usadas e restantes de um participante da promoção |
| [**instantAwardTryToWin()**](InstantAwardsApi.md#instantAwardTryToWin) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/try_to_win | Realiza a tentativa de ganho de um prêmio instantâneo para o participante da promoção |


## `instantAwardAttempts()`

```php
instantAwardAttempts($promotion_id, $user_id): \IdpluggerPromotion\Model\InstantAwardAttempts200Response
```

Retorna a quantidade de chances usadas e restantes de um participante da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\InstantAwardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário

try {
    $result = $apiInstance->instantAwardAttempts($promotion_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantAwardsApi->instantAwardAttempts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |

### Return type

[**\IdpluggerPromotion\Model\InstantAwardAttempts200Response**](../Model/InstantAwardAttempts200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `instantAwardTryToWin()`

```php
instantAwardTryToWin($promotion_id, $user_id): \IdpluggerPromotion\Model\InstantAwardTryToWin200Response
```

Realiza a tentativa de ganho de um prêmio instantâneo para o participante da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\InstantAwardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário

try {
    $result = $apiInstance->instantAwardTryToWin($promotion_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantAwardsApi->instantAwardTryToWin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |

### Return type

[**\IdpluggerPromotion\Model\InstantAwardTryToWin200Response**](../Model/InstantAwardTryToWin200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
