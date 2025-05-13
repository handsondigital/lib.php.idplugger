# IdpluggerPromotion\AwardedsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**awardedsSearch()**](AwardedsApi.md#awardedsSearch) | **GET** /v3/promotion/{promotion_id}/awardeds | Busca por usuários cadastrados na promoção ganhadores de sorteios |
| [**awardedsStates()**](AwardedsApi.md#awardedsStates) | **GET** /v3/promotion/{promotion_id}/awardeds/states | Lista os status de ganhador existentes na promoção |
| [**awardedsUpdate()**](AwardedsApi.md#awardedsUpdate) | **PATCH** /v3/promotion/{promotion_id}/awardeds | Atualiza informações referentes aos ganhadores de sorteios da promoção |


## `awardedsSearch()`

```php
awardedsSearch($promotion_id, $_fields, $_include, $user_id, $lucky_number_id, $checklist, $justificativa): \IdpluggerPromotion\Model\AwardedsSearch200Response
```

Busca por usuários cadastrados na promoção ganhadores de sorteios

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AwardedsApi(
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
    $result = $apiInstance->awardedsSearch($promotion_id, $_fields, $_include, $user_id, $lucky_number_id, $checklist, $justificativa);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AwardedsApi->awardedsSearch: ', $e->getMessage(), PHP_EOL;
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

[**\IdpluggerPromotion\Model\AwardedsSearch200Response**](../Model/AwardedsSearch200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `awardedsStates()`

```php
awardedsStates($promotion_id): \IdpluggerPromotion\Model\AwardedsStates200Response
```

Lista os status de ganhador existentes na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AwardedsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção

try {
    $result = $apiInstance->awardedsStates($promotion_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AwardedsApi->awardedsStates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |

### Return type

[**\IdpluggerPromotion\Model\AwardedsStates200Response**](../Model/AwardedsStates200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `awardedsUpdate()`

```php
awardedsUpdate($promotion_id): \IdpluggerPromotion\Model\AwardedsUpdate200Response
```

Atualiza informações referentes aos ganhadores de sorteios da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AwardedsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção

try {
    $result = $apiInstance->awardedsUpdate($promotion_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AwardedsApi->awardedsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |

### Return type

[**\IdpluggerPromotion\Model\AwardedsUpdate200Response**](../Model/AwardedsUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
