# IdpluggerPromotion\CouponsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**couponsCreate()**](CouponsApi.md#couponsCreate) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra um cupom para um usuário cadastrado na promoção |
| [**couponsDelete()**](CouponsApi.md#couponsDelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id}/coupons/{coupon_id} | Exclui um cupom de um usuário cadastrado na promoção |
| [**couponsIndex()**](CouponsApi.md#couponsIndex) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Busca por cupons de um usuário cadastrado na promoção |
| [**couponsUpdate()**](CouponsApi.md#couponsUpdate) | **PATCH** /v3/promotion/{promotion_id}/users/{user_id}/coupons | Cadastra ou atualiza um cupom para um usuário cadastrado na promoção |
| [**cuponsWebhook()**](CouponsApi.md#cuponsWebhook) | **POST** /webhook-do-cupom | Webhook de resposta ao registro de cupons |
| [**v3PromotionPromotionIdCouponsGet()**](CouponsApi.md#v3PromotionPromotionIdCouponsGet) | **GET** /v3/promotion/{promotion_id}/coupons | Buscar cupons de uma promoção |


## `couponsCreate()`

```php
couponsCreate($promotion_id, $user_id, $coupons_create_request): \IdpluggerPromotion\Model\CouponsCreate200Response
```

Cadastra um cupom para um usuário cadastrado na promoção

Os registros de cupons são processados individualmente e o resultado é enviado via webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\CouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$coupons_create_request = new \IdpluggerPromotion\Model\CouponsCreateRequest(); // \IdpluggerPromotion\Model\CouponsCreateRequest

try {
    $result = $apiInstance->couponsCreate($promotion_id, $user_id, $coupons_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponsApi->couponsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **coupons_create_request** | [**\IdpluggerPromotion\Model\CouponsCreateRequest**](../Model/CouponsCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\CouponsCreate200Response**](../Model/CouponsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `couponsDelete()`

```php
couponsDelete($promotion_id, $user_id, $coupon_id): \IdpluggerPromotion\Model\CouponsDelete200Response
```

Exclui um cupom de um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\CouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário
$coupon_id = 'coupon_id_example'; // string | ID do cupom

try {
    $result = $apiInstance->couponsDelete($promotion_id, $user_id, $coupon_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponsApi->couponsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |
| **coupon_id** | **string**| ID do cupom | |

### Return type

[**\IdpluggerPromotion\Model\CouponsDelete200Response**](../Model/CouponsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `couponsIndex()`

```php
couponsIndex($promotion_id, $user_id, $_fields, $_include, $page, $_per_page, $id, $user_id2, $external_user_id): \IdpluggerPromotion\Model\V3PromotionPromotionIdCouponsGet200Response
```

Busca por cupons de um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\CouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$_fields = ["id"]; // string | Campos a serem retornados
$_include = ["custom_data,coupon,lucky_numbers"]; // string | Campos a serem retornados
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$id = 'id_example'; // string | Id do cupom
$user_id2 = 'user_id_example'; // string | Id do usuário associado ao cupom
$external_user_id = 'external_user_id_example'; // string | Id externo do usuário associado ao cupom

try {
    $result = $apiInstance->couponsIndex($promotion_id, $user_id, $_fields, $_include, $page, $_per_page, $id, $user_id2, $external_user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponsApi->couponsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Campos a serem retornados | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **id** | **string**| Id do cupom | [optional] |
| **user_id2** | **string**| Id do usuário associado ao cupom | [optional] |
| **external_user_id** | **string**| Id externo do usuário associado ao cupom | [optional] |

### Return type

[**\IdpluggerPromotion\Model\V3PromotionPromotionIdCouponsGet200Response**](../Model/V3PromotionPromotionIdCouponsGet200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `couponsUpdate()`

```php
couponsUpdate($promotion_id, $user_id, $coupons_create_request): \IdpluggerPromotion\Model\CouponsUpdate201Response
```

Cadastra ou atualiza um cupom para um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\CouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 56; // int | ID do usuário
$coupons_create_request = new \IdpluggerPromotion\Model\CouponsCreateRequest(); // \IdpluggerPromotion\Model\CouponsCreateRequest

try {
    $result = $apiInstance->couponsUpdate($promotion_id, $user_id, $coupons_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponsApi->couponsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **int**| ID do usuário | |
| **coupons_create_request** | [**\IdpluggerPromotion\Model\CouponsCreateRequest**](../Model/CouponsCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\CouponsUpdate201Response**](../Model/CouponsUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cuponsWebhook()`

```php
cuponsWebhook($cupons_webhook_request): \IdpluggerPromotion\Model\UsersWebhook200Response
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
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\CouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cupons_webhook_request = new \IdpluggerPromotion\Model\CuponsWebhookRequest(); // \IdpluggerPromotion\Model\CuponsWebhookRequest

$hostIndex = 0;
$variables = [
];

try {
    $result = $apiInstance->cuponsWebhook($cupons_webhook_request, $hostIndex, $variables);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponsApi->cuponsWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cupons_webhook_request** | [**\IdpluggerPromotion\Model\CuponsWebhookRequest**](../Model/CuponsWebhookRequest.md)|  | [optional] |
| hostIndex | null|int | Host index. Defaults to null. If null, then the library will use $this->hostIndex instead | [optional] |
| variables | array | Associative array of variables to pass to the host. Defaults to empty array. | [optional] |

### Return type

[**\IdpluggerPromotion\Model\UsersWebhook200Response**](../Model/UsersWebhook200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v3PromotionPromotionIdCouponsGet()`

```php
v3PromotionPromotionIdCouponsGet($promotion_id, $_fields, $_include, $page, $_per_page, $id, $user_id, $external_user_id, $purchase_date, $insert_at, $tax_coupon): \IdpluggerPromotion\Model\V3PromotionPromotionIdCouponsGet200Response
```

Buscar cupons de uma promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\CouponsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,taxcoupon; // string
$_include = custom_data,lucky_numbers,serial_numbers,products; // string
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$id = 1; // int
$user_id = 1; // int
$external_user_id = user_1; // string
$purchase_date = 2025-06-13 00:00:00 AND 2025-06-13 23:59:59; // string
$insert_at = 2025-06-23 00:00:00 AND 2025-06-23 23:59:59; // string
$tax_coupon = 160630; // int

try {
    $result = $apiInstance->v3PromotionPromotionIdCouponsGet($promotion_id, $_fields, $_include, $page, $_per_page, $id, $user_id, $external_user_id, $purchase_date, $insert_at, $tax_coupon);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponsApi->v3PromotionPromotionIdCouponsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**|  | [optional] |
| **_include** | **string**|  | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **id** | **int**|  | [optional] |
| **user_id** | **int**|  | [optional] |
| **external_user_id** | **string**|  | [optional] |
| **purchase_date** | **string**|  | [optional] |
| **insert_at** | **string**|  | [optional] |
| **tax_coupon** | **int**|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\V3PromotionPromotionIdCouponsGet200Response**](../Model/V3PromotionPromotionIdCouponsGet200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
