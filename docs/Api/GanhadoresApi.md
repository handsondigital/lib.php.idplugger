# IdPluggerPromotion\GanhadoresApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionAwardedsSearch()**](GanhadoresApi.md#promotionAwardedsSearch) | **GET** /v3/promotion/{promotion_id}/awardeds | Busca por usuários cadastrados na promoção ganhadores de sorteios |
| [**promotionAwardedsStates()**](GanhadoresApi.md#promotionAwardedsStates) | **GET** /v3/promotion/{promotion_id}/awardeds/states | Lista os status de ganhador existentes na promoção |
| [**promotionAwardedsUpdate()**](GanhadoresApi.md#promotionAwardedsUpdate) | **PATCH** /v3/promotion/{promotion_id}/awardeds | Atualiza informações referentes aos ganhadores de sorteios da promoção |


## `promotionAwardedsSearch()`

```php
promotionAwardedsSearch($promotion_id, $_fields, $_include, $user_id, $lucky_number_id, $checklist, $justificativa): \IdPluggerPromotion\Model\PromotionAwardedsSearch200Response
```

Busca por usuários cadastrados na promoção ganhadores de sorteios

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\GanhadoresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = user,lucky_number,award,award_state; // string | Campos a serem retornados
$_include = user,lucky_number,award,award_state; // string | Dados relacionados a serem retornados
$user_id = 1; // string | Id do usuário
$lucky_number_id = 1; // string | Id do número da sorte
$checklist = 'checklist_example'; // string | Busca ganhadores pelo texto do checklist
$justificativa = 'justificativa_example'; // string | Busca ganhadores pelo texto da justificativa

try {
    $result = $apiInstance->promotionAwardedsSearch($promotion_id, $_fields, $_include, $user_id, $lucky_number_id, $checklist, $justificativa);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GanhadoresApi->promotionAwardedsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Dados relacionados a serem retornados | [optional] |
| **user_id** | **string**| Id do usuário | [optional] |
| **lucky_number_id** | **string**| Id do número da sorte | [optional] |
| **checklist** | **string**| Busca ganhadores pelo texto do checklist | [optional] |
| **justificativa** | **string**| Busca ganhadores pelo texto da justificativa | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionAwardedsSearch200Response**](../Model/PromotionAwardedsSearch200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionAwardedsStates()`

```php
promotionAwardedsStates($promotion_id): \IdPluggerPromotion\Model\PromotionAwardedsStates200Response
```

Lista os status de ganhador existentes na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\GanhadoresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção

try {
    $result = $apiInstance->promotionAwardedsStates($promotion_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GanhadoresApi->promotionAwardedsStates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |

### Return type

[**\IdPluggerPromotion\Model\PromotionAwardedsStates200Response**](../Model/PromotionAwardedsStates200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionAwardedsUpdate()`

```php
promotionAwardedsUpdate($promotion_id): \IdPluggerPromotion\Model\PromotionAwardedsUpdate200Response
```

Atualiza informações referentes aos ganhadores de sorteios da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\GanhadoresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção

try {
    $result = $apiInstance->promotionAwardedsUpdate($promotion_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GanhadoresApi->promotionAwardedsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |

### Return type

[**\IdPluggerPromotion\Model\PromotionAwardedsUpdate200Response**](../Model/PromotionAwardedsUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
