# IdpluggerPromotion\TicketsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**ticketsCreate()**](TicketsApi.md#ticketsCreate) | **POST** /v3/promotion/{promotion_id}/tickets | Cadastra um ticket de suporte na promoção |
| [**ticketsDelete()**](TicketsApi.md#ticketsDelete) | **DELETE** /v3/promotion/{promotion_id}/tickets/{id} | Exclui um ticket de suporte da promoção |
| [**ticketsIndex()**](TicketsApi.md#ticketsIndex) | **GET** /v3/promotion/{promotion_id}/tickets | Busca por tickets de suporte cadastrados na promoção |
| [**ticketsUpdate()**](TicketsApi.md#ticketsUpdate) | **PATCH** /v3/promotion/{promotion_id}/tickets | Cadastra ou atualiza um ticket de suporte na promoção |


## `ticketsCreate()`

```php
ticketsCreate($promotion_id, $ticket): \IdpluggerPromotion\Model\TicketsCreate200Response
```

Cadastra um ticket de suporte na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$ticket = array(new \IdpluggerPromotion\Model\Ticket()); // \IdpluggerPromotion\Model\Ticket[]

try {
    $result = $apiInstance->ticketsCreate($promotion_id, $ticket);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->ticketsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **ticket** | [**\IdpluggerPromotion\Model\Ticket[]**](../Model/Ticket.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\TicketsCreate200Response**](../Model/TicketsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ticketsDelete()`

```php
ticketsDelete($promotion_id, $id): \IdpluggerPromotion\Model\TicketsDelete200Response
```

Exclui um ticket de suporte da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do ticket de suporte

try {
    $result = $apiInstance->ticketsDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->ticketsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do ticket de suporte | |

### Return type

[**\IdpluggerPromotion\Model\TicketsDelete200Response**](../Model/TicketsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ticketsIndex()`

```php
ticketsIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $parent_id, $user_from_id, $user_to_id, $status, $search): \IdpluggerPromotion\Model\TicketsIndex200Response
```

Busca por tickets de suporte cadastrados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,assunto,content; // string | Dados associados
$_include = source,parent,from,to,lastUser; // string | Dados associados
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$id = 'id_example'; // string | Id do ticket
$parent_id = 'parent_id_example'; // string | Id do ticket que gerou a resposta
$user_from_id = 'user_from_id_example'; // string | Id do remetente
$user_to_id = 'user_to_id_example'; // string | Id do destinatário
$status = 'status_example'; // string | Status do destinatário
$search = 'search_example'; // string | Texto para pesquisa por nome/email do participante

try {
    $result = $apiInstance->ticketsIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $parent_id, $user_from_id, $user_to_id, $status, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->ticketsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Dados associados | [optional] |
| **_include** | **string**| Dados associados | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **id** | **string**| Id do ticket | [optional] |
| **parent_id** | **string**| Id do ticket que gerou a resposta | [optional] |
| **user_from_id** | **string**| Id do remetente | [optional] |
| **user_to_id** | **string**| Id do destinatário | [optional] |
| **status** | **string**| Status do destinatário | [optional] |
| **search** | **string**| Texto para pesquisa por nome/email do participante | [optional] |

### Return type

[**\IdpluggerPromotion\Model\TicketsIndex200Response**](../Model/TicketsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ticketsUpdate()`

```php
ticketsUpdate($promotion_id, $ticket): \IdpluggerPromotion\Model\TicketsUpdate200Response
```

Cadastra ou atualiza um ticket de suporte na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$ticket = {}; // \IdpluggerPromotion\Model\Ticket[]

try {
    $result = $apiInstance->ticketsUpdate($promotion_id, $ticket);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->ticketsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **ticket** | [**\IdpluggerPromotion\Model\Ticket[]**](../Model/Ticket.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\TicketsUpdate200Response**](../Model/TicketsUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
