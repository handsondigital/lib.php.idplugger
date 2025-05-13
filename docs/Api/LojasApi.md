# IdPluggerPromotion\LojasApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionStoresCreate()**](LojasApi.md#promotionStoresCreate) | **POST** /v3/promotion/{promotion_id}/stores | Cadastra uma loja na promoção |
| [**promotionStoresIndex()**](LojasApi.md#promotionStoresIndex) | **GET** /v3/promotion/{promotion_id}/stores | Busca por lojas cadastradas na promoção |
| [**promotionStoresUpdate()**](LojasApi.md#promotionStoresUpdate) | **PATCH** /v3/promotion/{promotion_id}/stores | Cadastra ou atualiza lojas na promoção |


## `promotionStoresCreate()`

```php
promotionStoresCreate($promotion_id, $promotion_stores_create_request): \IdPluggerPromotion\Model\PromotionStoresCreate200Response
```

Cadastra uma loja na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\LojasApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_stores_create_request = new \IdPluggerPromotion\Model\PromotionStoresCreateRequest(); // \IdPluggerPromotion\Model\PromotionStoresCreateRequest

try {
    $result = $apiInstance->promotionStoresCreate($promotion_id, $promotion_stores_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LojasApi->promotionStoresCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_stores_create_request** | [**\IdPluggerPromotion\Model\PromotionStoresCreateRequest**](../Model/PromotionStoresCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionStoresCreate200Response**](../Model/PromotionStoresCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionStoresIndex()`

```php
promotionStoresIndex($promotion_id, $_fields, $_include, $id, $cnpj): \IdPluggerPromotion\Model\PromotionStoresIndex200Response
```

Busca por lojas cadastradas na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\LojasApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = ["id"]; // string | Campos a serem retornados
$_include = ["coupons"]; // string | Associações a serem retornadas
$id = 'id_example'; // string | Id da loja
$cnpj = 'cnpj_example'; // string | CNPJ da loja

try {
    $result = $apiInstance->promotionStoresIndex($promotion_id, $_fields, $_include, $id, $cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LojasApi->promotionStoresIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Associações a serem retornadas | [optional] |
| **id** | **string**| Id da loja | [optional] |
| **cnpj** | **string**| CNPJ da loja | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionStoresIndex200Response**](../Model/PromotionStoresIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionStoresUpdate()`

```php
promotionStoresUpdate($promotion_id, $promotion_stores_create_request): \IdPluggerPromotion\Model\PromotionStoresUpdate201Response
```

Cadastra ou atualiza lojas na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\LojasApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_stores_create_request = new \IdPluggerPromotion\Model\PromotionStoresCreateRequest(); // \IdPluggerPromotion\Model\PromotionStoresCreateRequest

try {
    $result = $apiInstance->promotionStoresUpdate($promotion_id, $promotion_stores_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LojasApi->promotionStoresUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_stores_create_request** | [**\IdPluggerPromotion\Model\PromotionStoresCreateRequest**](../Model/PromotionStoresCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionStoresUpdate201Response**](../Model/PromotionStoresUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
