# IdpluggerPromotion\LuckyNumbersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**luckyNumbersAddCustom()**](LuckyNumbersApi.md#luckyNumbersAddCustom) | **POST** /v3/promotion/{promotion_id}/lucky_numbers | Cadastra Números da Sorte no repositório da promoção |
| [**luckyNumbersRemove()**](LuckyNumbersApi.md#luckyNumbersRemove) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers/remove | Inativa e remove Números da Sorte cadastrados na promoção |
| [**luckyNumbersSearch()**](LuckyNumbersApi.md#luckyNumbersSearch) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers | Busca por Números da Sorte de um usuário cadastrado na promoção |


## `luckyNumbersAddCustom()`

```php
luckyNumbersAddCustom($promotion_id, $add_lucky_number_custom): \IdpluggerPromotion\Model\LuckyNumbersAddCustom200Response
```

Cadastra Números da Sorte no repositório da promoção

Os Números da Sorte cadastrados através deste endpoint serão distribuidos aos participantes de acordo com as regras da promoção. Só é possível cadastrar números da sorte quando as regras da promoção permitem.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\LuckyNumbersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$add_lucky_number_custom = new \IdpluggerPromotion\Model\AddLuckyNumberCustom(); // \IdpluggerPromotion\Model\AddLuckyNumberCustom

try {
    $result = $apiInstance->luckyNumbersAddCustom($promotion_id, $add_lucky_number_custom);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LuckyNumbersApi->luckyNumbersAddCustom: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **add_lucky_number_custom** | [**\IdpluggerPromotion\Model\AddLuckyNumberCustom**](../Model/AddLuckyNumberCustom.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\LuckyNumbersAddCustom200Response**](../Model/LuckyNumbersAddCustom200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `luckyNumbersRemove()`

```php
luckyNumbersRemove($promotion_id, $user_id, $lucky_numbers_remove_request): \IdpluggerPromotion\Model\LuckyNumbersRemove200Response
```

Inativa e remove Números da Sorte cadastrados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\LuckyNumbersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$lucky_numbers_remove_request = new \IdpluggerPromotion\Model\LuckyNumbersRemoveRequest(); // \IdpluggerPromotion\Model\LuckyNumbersRemoveRequest

try {
    $result = $apiInstance->luckyNumbersRemove($promotion_id, $user_id, $lucky_numbers_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LuckyNumbersApi->luckyNumbersRemove: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **lucky_numbers_remove_request** | [**\IdpluggerPromotion\Model\LuckyNumbersRemoveRequest**](../Model/LuckyNumbersRemoveRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\LuckyNumbersRemove200Response**](../Model/LuckyNumbersRemove200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `luckyNumbersSearch()`

```php
luckyNumbersSearch($promotion_id, $user_id, $_fields, $page, $_per_page, $id, $coupon_id, $lucky_number, $serie, $situation, $serial_number_id): \IdpluggerPromotion\Model\LuckyNumbersSearch200Response
```

Busca por Números da Sorte de um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\LuckyNumbersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$_fields = '_fields_example'; // string | Campos a serem retornados
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$id = 'id_example'; // string | Id do número da sorte
$coupon_id = 'coupon_id_example'; // string | Id do cupom associado ao número da sorte
$lucky_number = 'lucky_number_example'; // string | Número da sorte
$serie = 'serie_example'; // string | Série
$situation = 'situation_example'; // string | Situação do número da sorte
$serial_number_id = 'serial_number_id_example'; // string | Id do serial associado ao número da sorte

try {
    $result = $apiInstance->luckyNumbersSearch($promotion_id, $user_id, $_fields, $page, $_per_page, $id, $coupon_id, $lucky_number, $serie, $situation, $serial_number_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LuckyNumbersApi->luckyNumbersSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **id** | **string**| Id do número da sorte | [optional] |
| **coupon_id** | **string**| Id do cupom associado ao número da sorte | [optional] |
| **lucky_number** | **string**| Número da sorte | [optional] |
| **serie** | **string**| Série | [optional] |
| **situation** | **string**| Situação do número da sorte | [optional] |
| **serial_number_id** | **string**| Id do serial associado ao número da sorte | [optional] |

### Return type

[**\IdpluggerPromotion\Model\LuckyNumbersSearch200Response**](../Model/LuckyNumbersSearch200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
