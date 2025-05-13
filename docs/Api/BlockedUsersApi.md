# IdpluggerPromotion\BlockedUsersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**blacklistCreate()**](BlockedUsersApi.md#blacklistCreate) | **POST** /v3/promotion/{promotion_id}/users/blacklist | Cadastra um CPF na lista de CPFs bloqueados na promoção |
| [**blacklistDelete()**](BlockedUsersApi.md#blacklistDelete) | **DELETE** /v3/promotion/{promotion_id}/users/blacklist/{id} | Exclui um CPF da lista de CPFs bloqueados da promoção |
| [**blacklistIndex()**](BlockedUsersApi.md#blacklistIndex) | **GET** /v3/promotion/{promotion_id}/users/blacklist | Pesquisa por CPFs bloqueados na promoção |


## `blacklistCreate()`

```php
blacklistCreate($promotion_id, $blacklist_create_request): \IdpluggerPromotion\Model\BlacklistCreate200Response
```

Cadastra um CPF na lista de CPFs bloqueados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\BlockedUsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$blacklist_create_request = new \IdpluggerPromotion\Model\BlacklistCreateRequest(); // \IdpluggerPromotion\Model\BlacklistCreateRequest

try {
    $result = $apiInstance->blacklistCreate($promotion_id, $blacklist_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockedUsersApi->blacklistCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **blacklist_create_request** | [**\IdpluggerPromotion\Model\BlacklistCreateRequest**](../Model/BlacklistCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\BlacklistCreate200Response**](../Model/BlacklistCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `blacklistDelete()`

```php
blacklistDelete($promotion_id, $id): \IdpluggerPromotion\Model\BlacklistDelete200Response
```

Exclui um CPF da lista de CPFs bloqueados da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\BlockedUsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do CPF bloqueado na promoção

try {
    $result = $apiInstance->blacklistDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockedUsersApi->blacklistDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do CPF bloqueado na promoção | |

### Return type

[**\IdpluggerPromotion\Model\BlacklistDelete200Response**](../Model/BlacklistDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `blacklistIndex()`

```php
blacklistIndex($promotion_id, $_fields, $cpf): \IdpluggerPromotion\Model\BlacklistIndex200Response
```

Pesquisa por CPFs bloqueados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\BlockedUsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,cpf,created_at; // string | Campos a serem retornados
$cpf = 'cpf_example'; // string | CPF bloqueado

try {
    $result = $apiInstance->blacklistIndex($promotion_id, $_fields, $cpf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockedUsersApi->blacklistIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **cpf** | **string**| CPF bloqueado | [optional] |

### Return type

[**\IdpluggerPromotion\Model\BlacklistIndex200Response**](../Model/BlacklistIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
