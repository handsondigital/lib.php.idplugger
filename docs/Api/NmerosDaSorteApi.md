# IdPluggerPromotion\NmerosDaSorteApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionLuckyNumbersAddCustom()**](NmerosDaSorteApi.md#promotionLuckyNumbersAddCustom) | **POST** /v3/promotion/{promotion_id}/lucky_numbers | Cadastra Números da Sorte no repositório da promoção |
| [**promotionLuckyNumbersRemove()**](NmerosDaSorteApi.md#promotionLuckyNumbersRemove) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers/remove | Inativa e remove Números da Sorte cadastrados na promoção |
| [**promotionLuckyNumbersSearch()**](NmerosDaSorteApi.md#promotionLuckyNumbersSearch) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/lucky_numbers | Busca por Números da Sorte de um usuário cadastrado na promoção |


## `promotionLuckyNumbersAddCustom()`

```php
promotionLuckyNumbersAddCustom($promotion_id, $add_lucky_number_custom): \IdPluggerPromotion\Model\PromotionLuckyNumbersAddCustom200Response
```

Cadastra Números da Sorte no repositório da promoção

Os Números da Sorte cadastrados através deste endpoint serão distribuidos aos participantes de acordo com as regras da promoção. Só é possível cadastrar números da sorte quando as regras da promoção permitem.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\NmerosDaSorteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$add_lucky_number_custom = new \IdPluggerPromotion\Model\AddLuckyNumberCustom(); // \IdPluggerPromotion\Model\AddLuckyNumberCustom

try {
    $result = $apiInstance->promotionLuckyNumbersAddCustom($promotion_id, $add_lucky_number_custom);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NmerosDaSorteApi->promotionLuckyNumbersAddCustom: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **add_lucky_number_custom** | [**\IdPluggerPromotion\Model\AddLuckyNumberCustom**](../Model/AddLuckyNumberCustom.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionLuckyNumbersAddCustom200Response**](../Model/PromotionLuckyNumbersAddCustom200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionLuckyNumbersRemove()`

```php
promotionLuckyNumbersRemove($promotion_id, $user_id, $promotion_lucky_numbers_remove_request): \IdPluggerPromotion\Model\PromotionLuckyNumbersRemove200Response
```

Inativa e remove Números da Sorte cadastrados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\NmerosDaSorteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$promotion_lucky_numbers_remove_request = new \IdPluggerPromotion\Model\PromotionLuckyNumbersRemoveRequest(); // \IdPluggerPromotion\Model\PromotionLuckyNumbersRemoveRequest

try {
    $result = $apiInstance->promotionLuckyNumbersRemove($promotion_id, $user_id, $promotion_lucky_numbers_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NmerosDaSorteApi->promotionLuckyNumbersRemove: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **promotion_lucky_numbers_remove_request** | [**\IdPluggerPromotion\Model\PromotionLuckyNumbersRemoveRequest**](../Model/PromotionLuckyNumbersRemoveRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionLuckyNumbersRemove200Response**](../Model/PromotionLuckyNumbersRemove200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionLuckyNumbersSearch()`

```php
promotionLuckyNumbersSearch($promotion_id, $user_id, $_fields, $id, $coupon_id, $lucky_number, $serie, $situation, $serial_number_id): \IdPluggerPromotion\Model\PromotionLuckyNumbersSearch200Response
```

Busca por Números da Sorte de um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\NmerosDaSorteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$_fields = '_fields_example'; // string | Campos a serem retornados
$id = 'id_example'; // string | Id do número da sorte
$coupon_id = 'coupon_id_example'; // string | Id do cupom associado ao número da sorte
$lucky_number = 'lucky_number_example'; // string | Número da sorte
$serie = 'serie_example'; // string | Série
$situation = 'situation_example'; // string | Situação do número da sorte
$serial_number_id = 'serial_number_id_example'; // string | Id do serial associado ao número da sorte

try {
    $result = $apiInstance->promotionLuckyNumbersSearch($promotion_id, $user_id, $_fields, $id, $coupon_id, $lucky_number, $serie, $situation, $serial_number_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NmerosDaSorteApi->promotionLuckyNumbersSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **id** | **string**| Id do número da sorte | [optional] |
| **coupon_id** | **string**| Id do cupom associado ao número da sorte | [optional] |
| **lucky_number** | **string**| Número da sorte | [optional] |
| **serie** | **string**| Série | [optional] |
| **situation** | **string**| Situação do número da sorte | [optional] |
| **serial_number_id** | **string**| Id do serial associado ao número da sorte | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionLuckyNumbersSearch200Response**](../Model/PromotionLuckyNumbersSearch200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
