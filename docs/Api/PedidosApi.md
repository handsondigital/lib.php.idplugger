# IdPluggerPromotion\PedidosApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionOrdersCreate()**](PedidosApi.md#promotionOrdersCreate) | **POST** /v3/promotion/{promotion_id}/users/{user_id}/orders | Cadastra um pedido para um usuário na promoção |
| [**promotionOrdersIndex()**](PedidosApi.md#promotionOrdersIndex) | **GET** /v3/promotion/{promotion_id}/users/{user_id}/orders | Pesquisa por pedidos na promoção |
| [**promotionOrdersUpdate()**](PedidosApi.md#promotionOrdersUpdate) | **PATCH** /v3/promotion/{promotion_id}/users/{user_id}/orders | Cadastra ou atualiza um pedido de um usuário na promoção |


## `promotionOrdersCreate()`

```php
promotionOrdersCreate($promotion_id, $user_id, $promotion_orders_create_request): \IdPluggerPromotion\Model\PromotionOrdersCreate200Response
```

Cadastra um pedido para um usuário na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\PedidosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário
$promotion_orders_create_request = new \IdPluggerPromotion\Model\PromotionOrdersCreateRequest(); // \IdPluggerPromotion\Model\PromotionOrdersCreateRequest

try {
    $result = $apiInstance->promotionOrdersCreate($promotion_id, $user_id, $promotion_orders_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PedidosApi->promotionOrdersCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |
| **promotion_orders_create_request** | [**\IdPluggerPromotion\Model\PromotionOrdersCreateRequest**](../Model/PromotionOrdersCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionOrdersCreate200Response**](../Model/PromotionOrdersCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionOrdersIndex()`

```php
promotionOrdersIndex($promotion_id, $user_id, $_fields, $_include, $id, $payment_id, $payment_gateway, $coupon_id, $status): \IdPluggerPromotion\Model\PromotionOrdersIndex200Response
```

Pesquisa por pedidos na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\PedidosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário
$_fields = ["id"]; // string | Campos a serem retornados
$_include = ["custom_data,coupon,lucky_numbers"]; // string | Campos a serem retornados
$id = 'id_example'; // string | Id do pedido
$payment_id = 'payment_id_example'; // string | ID do pagamento
$payment_gateway = 'payment_gateway_example'; // string | Gateway de pagamento do pedido
$coupon_id = 'coupon_id_example'; // string | ID do cupom do pedido
$status = 'status_example'; // string | Status do pedido

try {
    $result = $apiInstance->promotionOrdersIndex($promotion_id, $user_id, $_fields, $_include, $id, $payment_id, $payment_gateway, $coupon_id, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PedidosApi->promotionOrdersIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Campos a serem retornados | [optional] |
| **id** | **string**| Id do pedido | [optional] |
| **payment_id** | **string**| ID do pagamento | [optional] |
| **payment_gateway** | **string**| Gateway de pagamento do pedido | [optional] |
| **coupon_id** | **string**| ID do cupom do pedido | [optional] |
| **status** | **string**| Status do pedido | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionOrdersIndex200Response**](../Model/PromotionOrdersIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionOrdersUpdate()`

```php
promotionOrdersUpdate($promotion_id, $user_id, $promotion_orders_create_request): \IdPluggerPromotion\Model\PromotionOrdersUpdate200Response
```

Cadastra ou atualiza um pedido de um usuário na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\PedidosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário
$promotion_orders_create_request = new \IdPluggerPromotion\Model\PromotionOrdersCreateRequest(); // \IdPluggerPromotion\Model\PromotionOrdersCreateRequest

try {
    $result = $apiInstance->promotionOrdersUpdate($promotion_id, $user_id, $promotion_orders_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PedidosApi->promotionOrdersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |
| **promotion_orders_create_request** | [**\IdPluggerPromotion\Model\PromotionOrdersCreateRequest**](../Model/PromotionOrdersCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionOrdersUpdate200Response**](../Model/PromotionOrdersUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
