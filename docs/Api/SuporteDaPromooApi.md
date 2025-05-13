# IdPluggerPromotion\SuporteDaPromooApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionTicketsCreate()**](SuporteDaPromooApi.md#promotionTicketsCreate) | **POST** /v3/promotion/{promotion_id}/tickets | Cadastra um ticket de suporte na promoção |
| [**promotionTicketsDelete()**](SuporteDaPromooApi.md#promotionTicketsDelete) | **DELETE** /v3/promotion/{promotion_id}/tickets/{id} | Exclui um ticket de suporte da promoção |
| [**promotionTicketsIndex()**](SuporteDaPromooApi.md#promotionTicketsIndex) | **GET** /v3/promotion/{promotion_id}/tickets | Busca por tickets de suporte cadastrados na promoção |
| [**promotionTicketsUpdate()**](SuporteDaPromooApi.md#promotionTicketsUpdate) | **PATCH** /v3/promotion/{promotion_id}/tickets | Cadastra ou atualiza um ticket de suporte na promoção |


## `promotionTicketsCreate()`

```php
promotionTicketsCreate($promotion_id, $ticket): \IdPluggerPromotion\Model\PromotionTicketsCreate200Response
```

Cadastra um ticket de suporte na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SuporteDaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$ticket = array(new \IdPluggerPromotion\Model\Ticket()); // \IdPluggerPromotion\Model\Ticket[]

try {
    $result = $apiInstance->promotionTicketsCreate($promotion_id, $ticket);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuporteDaPromooApi->promotionTicketsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **ticket** | [**\IdPluggerPromotion\Model\Ticket[]**](../Model/Ticket.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionTicketsCreate200Response**](../Model/PromotionTicketsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionTicketsDelete()`

```php
promotionTicketsDelete($promotion_id, $id): \IdPluggerPromotion\Model\PromotionTicketsDelete200Response
```

Exclui um ticket de suporte da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SuporteDaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do ticket de suporte

try {
    $result = $apiInstance->promotionTicketsDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuporteDaPromooApi->promotionTicketsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do ticket de suporte | |

### Return type

[**\IdPluggerPromotion\Model\PromotionTicketsDelete200Response**](../Model/PromotionTicketsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionTicketsIndex()`

```php
promotionTicketsIndex($promotion_id, $_fields, $_include, $id, $parent_id, $user_from_id, $user_to_id, $status): \IdPluggerPromotion\Model\PromotionTicketsIndex200Response
```

Busca por tickets de suporte cadastrados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SuporteDaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,assunto,content; // string | Dados associados
$_include = source,parent,from,to,lastUser; // string | Dados associados
$id = 'id_example'; // string | Id do ticket
$parent_id = 'parent_id_example'; // string | Id do ticket que gerou a resposta
$user_from_id = 'user_from_id_example'; // string | Id do remetente
$user_to_id = 'user_to_id_example'; // string | Id do destinatário
$status = 'status_example'; // string | Status do destinatário

try {
    $result = $apiInstance->promotionTicketsIndex($promotion_id, $_fields, $_include, $id, $parent_id, $user_from_id, $user_to_id, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuporteDaPromooApi->promotionTicketsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Dados associados | [optional] |
| **_include** | **string**| Dados associados | [optional] |
| **id** | **string**| Id do ticket | [optional] |
| **parent_id** | **string**| Id do ticket que gerou a resposta | [optional] |
| **user_from_id** | **string**| Id do remetente | [optional] |
| **user_to_id** | **string**| Id do destinatário | [optional] |
| **status** | **string**| Status do destinatário | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionTicketsIndex200Response**](../Model/PromotionTicketsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionTicketsUpdate()`

```php
promotionTicketsUpdate($promotion_id, $ticket): \IdPluggerPromotion\Model\PromotionTicketsUpdate200Response
```

Cadastra ou atualiza um ticket de suporte na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\SuporteDaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$ticket = {}; // \IdPluggerPromotion\Model\Ticket[]

try {
    $result = $apiInstance->promotionTicketsUpdate($promotion_id, $ticket);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuporteDaPromooApi->promotionTicketsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **ticket** | [**\IdPluggerPromotion\Model\Ticket[]**](../Model/Ticket.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionTicketsUpdate200Response**](../Model/PromotionTicketsUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
