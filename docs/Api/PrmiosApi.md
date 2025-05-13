# IdPluggerPromotion\PrmiosApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionAwardsCreate()**](PrmiosApi.md#promotionAwardsCreate) | **POST** /v3/promotion/{promotion_id}/awards | Cadastra um prêmio na promoção |
| [**promotionAwardsDelete()**](PrmiosApi.md#promotionAwardsDelete) | **DELETE** /v3/promotion/{promotion_id}/awards/{id} | Deleta um prêmio da promoção |
| [**promotionAwardsIndex()**](PrmiosApi.md#promotionAwardsIndex) | **GET** /v3/promotion/{promotion_id}/awards | Pesquisa por prêmios na promoção |
| [**promotionAwardsUpdate()**](PrmiosApi.md#promotionAwardsUpdate) | **PATCH** /v3/promotion/{promotion_id}/awards | Cadastra ou atualiza um prêmio na promoção |


## `promotionAwardsCreate()`

```php
promotionAwardsCreate($promotion_id, $award): \IdPluggerPromotion\Model\PromotionAwardsCreate200Response
```

Cadastra um prêmio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\PrmiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$award = array(new \IdPluggerPromotion\Model\Award()); // \IdPluggerPromotion\Model\Award[]

try {
    $result = $apiInstance->promotionAwardsCreate($promotion_id, $award);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrmiosApi->promotionAwardsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **award** | [**\IdPluggerPromotion\Model\Award[]**](../Model/Award.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionAwardsCreate200Response**](../Model/PromotionAwardsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionAwardsDelete()`

```php
promotionAwardsDelete($promotion_id, $id): \IdPluggerPromotion\Model\PromotionAwardsDelete200Response
```

Deleta um prêmio da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\PrmiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 'id_example'; // string | ID do prêmio

try {
    $result = $apiInstance->promotionAwardsDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrmiosApi->promotionAwardsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **string**| ID do prêmio | |

### Return type

[**\IdPluggerPromotion\Model\PromotionAwardsDelete200Response**](../Model/PromotionAwardsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionAwardsIndex()`

```php
promotionAwardsIndex($promotion_id, $_fields, $_include, $id, $raffle_id, $raffle_type): \IdPluggerPromotion\Model\PromotionAwardsIndex200Response
```

Pesquisa por prêmios na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\PrmiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,name,raffle_type; // string | Campos a serem retornados
$_include = raffles,lotterys,awardeds; // string | Dados relacionados a serem retornados
$id = 1; // string | Id do prêmio
$raffle_id = 1; // string | Id do sorteio
$raffle_type = normal; // string | Tipo do sorteio

try {
    $result = $apiInstance->promotionAwardsIndex($promotion_id, $_fields, $_include, $id, $raffle_id, $raffle_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrmiosApi->promotionAwardsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Dados relacionados a serem retornados | [optional] |
| **id** | **string**| Id do prêmio | [optional] |
| **raffle_id** | **string**| Id do sorteio | [optional] |
| **raffle_type** | **string**| Tipo do sorteio | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionAwardsIndex200Response**](../Model/PromotionAwardsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionAwardsUpdate()`

```php
promotionAwardsUpdate($promotion_id, $award): \IdPluggerPromotion\Model\PromotionAwardsUpdate200Response
```

Cadastra ou atualiza um prêmio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\PrmiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$award = array(new \IdPluggerPromotion\Model\Award()); // \IdPluggerPromotion\Model\Award[]

try {
    $result = $apiInstance->promotionAwardsUpdate($promotion_id, $award);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PrmiosApi->promotionAwardsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **award** | [**\IdPluggerPromotion\Model\Award[]**](../Model/Award.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionAwardsUpdate200Response**](../Model/PromotionAwardsUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
