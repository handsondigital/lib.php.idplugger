# IdPluggerPromotion\SorteiosApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionRafflesCreate()**](SorteiosApi.md#promotionRafflesCreate) | **POST** /v3/promotion/{promotion_id}/raffles | Cadastra um sorteio na promoção |
| [**promotionRafflesDelete()**](SorteiosApi.md#promotionRafflesDelete) | **DELETE** /v3/promotion/{promotion_id}/raffles/{id} | Exclui um sorteio da promoção |
| [**promotionRafflesIndex()**](SorteiosApi.md#promotionRafflesIndex) | **GET** /v3/promotion/{promotion_id}/raffles | Pesquisa por sorteios na promoção |
| [**promotionRafflesReport()**](SorteiosApi.md#promotionRafflesReport) | **POST** /v3/promotion/{promotion_id}/raffles/{id}/report | Envia por e-mail o relatório de cupons participantes de um sorteio |
| [**promotionRafflesUpdate()**](SorteiosApi.md#promotionRafflesUpdate) | **PATCH** /v3/promotion/{promotion_id}/raffles | Cadastra ou atualiza um sorteio na promoção |


## `promotionRafflesCreate()`

```php
promotionRafflesCreate($promotion_id, $promotion_raffles_create_request_inner): \IdPluggerPromotion\Model\PromotionRafflesCreate200Response
```

Cadastra um sorteio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SorteiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_raffles_create_request_inner = array(new \IdPluggerPromotion\Model\PromotionRafflesCreateRequestInner()); // \IdPluggerPromotion\Model\PromotionRafflesCreateRequestInner[]

try {
    $result = $apiInstance->promotionRafflesCreate($promotion_id, $promotion_raffles_create_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SorteiosApi->promotionRafflesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_raffles_create_request_inner** | [**\IdPluggerPromotion\Model\PromotionRafflesCreateRequestInner[]**](../Model/PromotionRafflesCreateRequestInner.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionRafflesCreate200Response**](../Model/PromotionRafflesCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionRafflesDelete()`

```php
promotionRafflesDelete($promotion_id, $id): \IdPluggerPromotion\Model\PromotionRafflesDelete200Response
```

Exclui um sorteio da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SorteiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do sorteio na promoção

try {
    $result = $apiInstance->promotionRafflesDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SorteiosApi->promotionRafflesDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do sorteio na promoção | |

### Return type

[**\IdPluggerPromotion\Model\PromotionRafflesDelete200Response**](../Model/PromotionRafflesDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionRafflesIndex()`

```php
promotionRafflesIndex($promotion_id, $_fields, $id, $raffle_date_start, $raffle_date_end, $raffle_date, $realizado_em, $status): \IdPluggerPromotion\Model\PromotionRafflesIndex200Response
```

Pesquisa por sorteios na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SorteiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = ["id"]; // string | Campos a serem retornados
$id = 'id_example'; // string | Id do pedido
$raffle_date_start = 2021-01-30 00:00:00 AND 2021-01-31 23:59:59; // string | Início da participação no sorteio
$raffle_date_end = 2021-02-15 00:00:00 AND 2021-02-16 23:59:59; // string | Fim da participação no sorteio
$raffle_date = 2021-02-20 00:00:00 AND 2021-02-25 23:59:59; // string | Data prevista para o sorteio
$realizado_em = 2021-02-20 00:00:00 AND 2021-02-25 23:59:59; // string | Data em que o sorteio foi realizado
$status = 1; // string | Pesquisa por um sorteio com determinado status

try {
    $result = $apiInstance->promotionRafflesIndex($promotion_id, $_fields, $id, $raffle_date_start, $raffle_date_end, $raffle_date, $realizado_em, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SorteiosApi->promotionRafflesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **id** | **string**| Id do pedido | [optional] |
| **raffle_date_start** | **string**| Início da participação no sorteio | [optional] |
| **raffle_date_end** | **string**| Fim da participação no sorteio | [optional] |
| **raffle_date** | **string**| Data prevista para o sorteio | [optional] |
| **realizado_em** | **string**| Data em que o sorteio foi realizado | [optional] |
| **status** | **string**| Pesquisa por um sorteio com determinado status | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionRafflesIndex200Response**](../Model/PromotionRafflesIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionRafflesReport()`

```php
promotionRafflesReport($promotion_id, $id, $promotion_raffles_report_request): \IdPluggerPromotion\Model\PromotionRafflesDelete200Response
```

Envia por e-mail o relatório de cupons participantes de um sorteio

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SorteiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do sorteio na promoção
$promotion_raffles_report_request = new \IdPluggerPromotion\Model\PromotionRafflesReportRequest(); // \IdPluggerPromotion\Model\PromotionRafflesReportRequest

try {
    $result = $apiInstance->promotionRafflesReport($promotion_id, $id, $promotion_raffles_report_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SorteiosApi->promotionRafflesReport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do sorteio na promoção | |
| **promotion_raffles_report_request** | [**\IdPluggerPromotion\Model\PromotionRafflesReportRequest**](../Model/PromotionRafflesReportRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionRafflesDelete200Response**](../Model/PromotionRafflesDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionRafflesUpdate()`

```php
promotionRafflesUpdate($promotion_id, $promotion_raffles_update_request_inner): \IdPluggerPromotion\Model\PromotionRafflesUpdate200Response
```

Cadastra ou atualiza um sorteio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SorteiosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_raffles_update_request_inner = array(new \IdPluggerPromotion\Model\PromotionRafflesUpdateRequestInner()); // \IdPluggerPromotion\Model\PromotionRafflesUpdateRequestInner[]

try {
    $result = $apiInstance->promotionRafflesUpdate($promotion_id, $promotion_raffles_update_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SorteiosApi->promotionRafflesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_raffles_update_request_inner** | [**\IdPluggerPromotion\Model\PromotionRafflesUpdateRequestInner[]**](../Model/PromotionRafflesUpdateRequestInner.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionRafflesUpdate200Response**](../Model/PromotionRafflesUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
