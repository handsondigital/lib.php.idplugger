# IdPluggerPromotion\CPFsBloqueadosApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionBlacklistCreate()**](CPFsBloqueadosApi.md#promotionBlacklistCreate) | **POST** /v3/promotion/{promotion_id}/users/blacklist | Cadastra um CPF na lista de CPFs bloqueados na promoção |
| [**promotionBlacklistDelete()**](CPFsBloqueadosApi.md#promotionBlacklistDelete) | **DELETE** /v3/promotion/{promotion_id}/users/blacklist/{id} | Exclui um CPF da lista de CPFs bloqueados da promoção |
| [**promotionBlacklistIndex()**](CPFsBloqueadosApi.md#promotionBlacklistIndex) | **GET** /v3/promotion/{promotion_id}/users/blacklist | Pesquisa por CPFs bloqueados na promoção |


## `promotionBlacklistCreate()`

```php
promotionBlacklistCreate($promotion_id, $promotion_blacklist_create_request): \IdPluggerPromotion\Model\PromotionBlacklistCreate200Response
```

Cadastra um CPF na lista de CPFs bloqueados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CPFsBloqueadosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_blacklist_create_request = new \IdPluggerPromotion\Model\PromotionBlacklistCreateRequest(); // \IdPluggerPromotion\Model\PromotionBlacklistCreateRequest

try {
    $result = $apiInstance->promotionBlacklistCreate($promotion_id, $promotion_blacklist_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPFsBloqueadosApi->promotionBlacklistCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_blacklist_create_request** | [**\IdPluggerPromotion\Model\PromotionBlacklistCreateRequest**](../Model/PromotionBlacklistCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionBlacklistCreate200Response**](../Model/PromotionBlacklistCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionBlacklistDelete()`

```php
promotionBlacklistDelete($promotion_id, $id): \IdPluggerPromotion\Model\PromotionBlacklistDelete200Response
```

Exclui um CPF da lista de CPFs bloqueados da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CPFsBloqueadosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do CPF bloqueado na promoção

try {
    $result = $apiInstance->promotionBlacklistDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPFsBloqueadosApi->promotionBlacklistDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do CPF bloqueado na promoção | |

### Return type

[**\IdPluggerPromotion\Model\PromotionBlacklistDelete200Response**](../Model/PromotionBlacklistDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionBlacklistIndex()`

```php
promotionBlacklistIndex($promotion_id, $_fields, $cpf): \IdPluggerPromotion\Model\PromotionBlacklistIndex200Response
```

Pesquisa por CPFs bloqueados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CPFsBloqueadosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,cpf,created_at; // string | Campos a serem retornados
$cpf = 'cpf_example'; // string | CPF bloqueado

try {
    $result = $apiInstance->promotionBlacklistIndex($promotion_id, $_fields, $cpf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPFsBloqueadosApi->promotionBlacklistIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **cpf** | **string**| CPF bloqueado | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionBlacklistIndex200Response**](../Model/PromotionBlacklistIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
