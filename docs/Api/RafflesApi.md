# IdpluggerPromotion\RafflesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**rafflesCreate()**](RafflesApi.md#rafflesCreate) | **POST** /v3/promotion/{promotion_id}/raffles | Cadastra um sorteio na promoção |
| [**rafflesDelete()**](RafflesApi.md#rafflesDelete) | **DELETE** /v3/promotion/{promotion_id}/raffles/{id} | Exclui um sorteio da promoção |
| [**rafflesIndex()**](RafflesApi.md#rafflesIndex) | **GET** /v3/promotion/{promotion_id}/raffles | Pesquisa por sorteios na promoção |
| [**rafflesReport()**](RafflesApi.md#rafflesReport) | **POST** /v3/promotion/{promotion_id}/raffles/{id}/report | Envia por e-mail o relatório de cupons participantes de um sorteio |
| [**rafflesUpdate()**](RafflesApi.md#rafflesUpdate) | **PATCH** /v3/promotion/{promotion_id}/raffles | Cadastra ou atualiza um sorteio na promoção |


## `rafflesCreate()`

```php
rafflesCreate($promotion_id, $raffles_create_request_inner): \IdpluggerPromotion\Model\RafflesCreate200Response
```

Cadastra um sorteio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\RafflesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$raffles_create_request_inner = array(new \IdpluggerPromotion\Model\RafflesCreateRequestInner()); // \IdpluggerPromotion\Model\RafflesCreateRequestInner[]

try {
    $result = $apiInstance->rafflesCreate($promotion_id, $raffles_create_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RafflesApi->rafflesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **raffles_create_request_inner** | [**\IdpluggerPromotion\Model\RafflesCreateRequestInner[]**](../Model/RafflesCreateRequestInner.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\RafflesCreate200Response**](../Model/RafflesCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rafflesDelete()`

```php
rafflesDelete($promotion_id, $id): \IdpluggerPromotion\Model\RafflesDelete200Response
```

Exclui um sorteio da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\RafflesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do sorteio na promoção

try {
    $result = $apiInstance->rafflesDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RafflesApi->rafflesDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do sorteio na promoção | |

### Return type

[**\IdpluggerPromotion\Model\RafflesDelete200Response**](../Model/RafflesDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rafflesIndex()`

```php
rafflesIndex($promotion_id, $_fields, $page, $_per_page, $id, $raffle_date_start, $raffle_date_end, $raffle_date, $realizado_em, $status): \IdpluggerPromotion\Model\RafflesIndex200Response
```

Pesquisa por sorteios na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\RafflesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = ["id"]; // string | Campos a serem retornados
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$id = 'id_example'; // string | Id do pedido
$raffle_date_start = 2021-01-30 00:00:00 AND 2021-01-31 23:59:59; // string | Início da participação no sorteio
$raffle_date_end = 2021-02-15 00:00:00 AND 2021-02-16 23:59:59; // string | Fim da participação no sorteio
$raffle_date = 2021-02-20 00:00:00 AND 2021-02-25 23:59:59; // string | Data prevista para o sorteio
$realizado_em = 2021-02-20 00:00:00 AND 2021-02-25 23:59:59; // string | Data em que o sorteio foi realizado
$status = 1; // string | Pesquisa por um sorteio com determinado status

try {
    $result = $apiInstance->rafflesIndex($promotion_id, $_fields, $page, $_per_page, $id, $raffle_date_start, $raffle_date_end, $raffle_date, $realizado_em, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RafflesApi->rafflesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **id** | **string**| Id do pedido | [optional] |
| **raffle_date_start** | **string**| Início da participação no sorteio | [optional] |
| **raffle_date_end** | **string**| Fim da participação no sorteio | [optional] |
| **raffle_date** | **string**| Data prevista para o sorteio | [optional] |
| **realizado_em** | **string**| Data em que o sorteio foi realizado | [optional] |
| **status** | **string**| Pesquisa por um sorteio com determinado status | [optional] |

### Return type

[**\IdpluggerPromotion\Model\RafflesIndex200Response**](../Model/RafflesIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rafflesReport()`

```php
rafflesReport($promotion_id, $id, $raffles_report_request): \IdpluggerPromotion\Model\RafflesDelete200Response
```

Envia por e-mail o relatório de cupons participantes de um sorteio

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\RafflesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do sorteio na promoção
$raffles_report_request = new \IdpluggerPromotion\Model\RafflesReportRequest(); // \IdpluggerPromotion\Model\RafflesReportRequest

try {
    $result = $apiInstance->rafflesReport($promotion_id, $id, $raffles_report_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RafflesApi->rafflesReport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do sorteio na promoção | |
| **raffles_report_request** | [**\IdpluggerPromotion\Model\RafflesReportRequest**](../Model/RafflesReportRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\RafflesDelete200Response**](../Model/RafflesDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rafflesUpdate()`

```php
rafflesUpdate($promotion_id, $raffles_update_request_inner): \IdpluggerPromotion\Model\RafflesUpdate200Response
```

Cadastra ou atualiza um sorteio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\RafflesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$raffles_update_request_inner = array(new \IdpluggerPromotion\Model\RafflesUpdateRequestInner()); // \IdpluggerPromotion\Model\RafflesUpdateRequestInner[]

try {
    $result = $apiInstance->rafflesUpdate($promotion_id, $raffles_update_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RafflesApi->rafflesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **raffles_update_request_inner** | [**\IdpluggerPromotion\Model\RafflesUpdateRequestInner[]**](../Model/RafflesUpdateRequestInner.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\RafflesUpdate200Response**](../Model/RafflesUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
