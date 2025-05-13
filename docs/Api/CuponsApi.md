# IdPluggerPromotion\CuponsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionCouponsCreate()**](CuponsApi.md#promotionCouponsCreate) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra um cupom para um usuário cadastrado na promoção |
| [**promotionCouponsDelete()**](CuponsApi.md#promotionCouponsDelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id}/coupons/{coupon_id} | Exclui um cupom de um usuário cadastrado na promoção |
| [**promotionCouponsIndex()**](CuponsApi.md#promotionCouponsIndex) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Busca por cupons de um usuário cadastrado na promoção |
| [**promotionCouponsUpdate()**](CuponsApi.md#promotionCouponsUpdate) | **PATCH** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra ou atualiza um cupom para um usuário cadastrado na promoção |
| [**promotionCuponsWebhook()**](CuponsApi.md#promotionCuponsWebhook) | **POST** /webhook-do-cupom | Webhook de resposta ao registro de cupons |


## `promotionCouponsCreate()`

```php
promotionCouponsCreate($promotion_id, $user_id, $promotion_coupons_create_request): \IdPluggerPromotion\Model\PromotionCouponsCreate200Response
```

Cadastra um cupom para um usuário cadastrado na promoção

Os registros de cupons são processados individualmente e o resultado é enviado via webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CuponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$promotion_coupons_create_request = new \IdPluggerPromotion\Model\PromotionCouponsCreateRequest(); // \IdPluggerPromotion\Model\PromotionCouponsCreateRequest

try {
    $result = $apiInstance->promotionCouponsCreate($promotion_id, $user_id, $promotion_coupons_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CuponsApi->promotionCouponsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **promotion_coupons_create_request** | [**\IdPluggerPromotion\Model\PromotionCouponsCreateRequest**](../Model/PromotionCouponsCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionCouponsCreate200Response**](../Model/PromotionCouponsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionCouponsDelete()`

```php
promotionCouponsDelete($promotion_id, $user_id, $coupon_id): \IdPluggerPromotion\Model\PromotionCouponsDelete200Response
```

Exclui um cupom de um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CuponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário
$coupon_id = 'coupon_id_example'; // string | ID do cupom

try {
    $result = $apiInstance->promotionCouponsDelete($promotion_id, $user_id, $coupon_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CuponsApi->promotionCouponsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |
| **coupon_id** | **string**| ID do cupom | |

### Return type

[**\IdPluggerPromotion\Model\PromotionCouponsDelete200Response**](../Model/PromotionCouponsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionCouponsIndex()`

```php
promotionCouponsIndex($promotion_id, $user_id, $_fields, $_include, $id, $user_id2, $external_user_id): \IdPluggerPromotion\Model\PromotionCouponsIndex200Response
```

Busca por cupons de um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CuponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$_fields = ["id"]; // string | Campos a serem retornados
$_include = ["custom_data,coupon,lucky_numbers"]; // string | Campos a serem retornados
$id = 'id_example'; // string | Id do cupom
$user_id2 = 'user_id_example'; // string | Id do usuário associado ao cupom
$external_user_id = 'external_user_id_example'; // string | Id externo do usuário associado ao cupom

try {
    $result = $apiInstance->promotionCouponsIndex($promotion_id, $user_id, $_fields, $_include, $id, $user_id2, $external_user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CuponsApi->promotionCouponsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Campos a serem retornados | [optional] |
| **id** | **string**| Id do cupom | [optional] |
| **user_id2** | **string**| Id do usuário associado ao cupom | [optional] |
| **external_user_id** | **string**| Id externo do usuário associado ao cupom | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionCouponsIndex200Response**](../Model/PromotionCouponsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionCouponsUpdate()`

```php
promotionCouponsUpdate($promotion_id, $user_id, $promotion_coupons_create_request): \IdPluggerPromotion\Model\PromotionCouponsUpdate201Response
```

Cadastra ou atualiza um cupom para um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CuponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$promotion_coupons_create_request = new \IdPluggerPromotion\Model\PromotionCouponsCreateRequest(); // \IdPluggerPromotion\Model\PromotionCouponsCreateRequest

try {
    $result = $apiInstance->promotionCouponsUpdate($promotion_id, $user_id, $promotion_coupons_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CuponsApi->promotionCouponsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **promotion_coupons_create_request** | [**\IdPluggerPromotion\Model\PromotionCouponsCreateRequest**](../Model/PromotionCouponsCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionCouponsUpdate201Response**](../Model/PromotionCouponsUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionCuponsWebhook()`

```php
promotionCuponsWebhook($promotion_cupons_webhook_request): \IdPluggerPromotion\Model\PromotionUsersWebhook200Response
```
### URI(s):
- https://api.example.com/ URL do servidor do cliente
Webhook de resposta ao registro de cupons

Este endpoint é apenas um exemplo de como você receberá em seu webhook a notificação do registro de um cupons na promoção.  Em **Request body** clique em **Schema** para ver todos as variações de requisições que a API faz.  Alguns erros são apenas informativos de que alguma parte não essencial do cadastro não funcionou. Para identificar se o cupons foi cadastrado ou não, verifique se o parâmetro `content.id` está incluso na requisição e é um número maior que zero.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\CuponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_cupons_webhook_request = new \IdPluggerPromotion\Model\PromotionCuponsWebhookRequest(); // \IdPluggerPromotion\Model\PromotionCuponsWebhookRequest

$hostIndex = 0;
$variables = [
];

try {
    $result = $apiInstance->promotionCuponsWebhook($promotion_cupons_webhook_request, $hostIndex, $variables);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CuponsApi->promotionCuponsWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_cupons_webhook_request** | [**\IdPluggerPromotion\Model\PromotionCuponsWebhookRequest**](../Model/PromotionCuponsWebhookRequest.md)|  | [optional] |
| hostIndex | null|int | Host index. Defaults to null. If null, then the library will use $this->hostIndex instead | [optional] |
| variables | array | Associative array of variables to pass to the host. Defaults to empty array. | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionUsersWebhook200Response**](../Model/PromotionUsersWebhook200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
