# IdpluggerPromotion\StoresApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storesCreate()**](StoresApi.md#storesCreate) | **POST** /v3/promotion/{promotion_id}/stores | Cadastra uma loja na promoção |
| [**storesDelete()**](StoresApi.md#storesDelete) | **DELETE** /v3/promotion/{promotion_id}/stores/{store_id} | Exclui um produto cadastrado na promoção |
| [**storesIndex()**](StoresApi.md#storesIndex) | **GET** /v3/promotion/{promotion_id}/stores | Busca por lojas cadastradas na promoção |
| [**storesUpdate()**](StoresApi.md#storesUpdate) | **PATCH** /v3/promotion/{promotion_id}/stores | Cadastra ou atualiza lojas na promoção |


## `storesCreate()`

```php
storesCreate($promotion_id, $stores_create_request): \IdpluggerPromotion\Model\StoresCreate200Response
```

Cadastra uma loja na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\StoresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$stores_create_request = new \IdpluggerPromotion\Model\StoresCreateRequest(); // \IdpluggerPromotion\Model\StoresCreateRequest

try {
    $result = $apiInstance->storesCreate($promotion_id, $stores_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresApi->storesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **stores_create_request** | [**\IdpluggerPromotion\Model\StoresCreateRequest**](../Model/StoresCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\StoresCreate200Response**](../Model/StoresCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesDelete()`

```php
storesDelete($promotion_id, $store_id): \IdpluggerPromotion\Model\StoresDelete200Response
```

Exclui um produto cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\StoresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$store_id = 'store_id_example'; // string | ID da loja

try {
    $result = $apiInstance->storesDelete($promotion_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresApi->storesDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **store_id** | **string**| ID da loja | |

### Return type

[**\IdpluggerPromotion\Model\StoresDelete200Response**](../Model/StoresDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesIndex()`

```php
storesIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $cnpj): \IdpluggerPromotion\Model\StoresIndex200Response
```

Busca por lojas cadastradas na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\StoresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = ["id"]; // string | Campos a serem retornados
$_include = ["coupons"]; // string | Associações a serem retornadas
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$id = 'id_example'; // string | Id da loja
$cnpj = 'cnpj_example'; // string | CNPJ da loja

try {
    $result = $apiInstance->storesIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresApi->storesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Associações a serem retornadas | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **id** | **string**| Id da loja | [optional] |
| **cnpj** | **string**| CNPJ da loja | [optional] |

### Return type

[**\IdpluggerPromotion\Model\StoresIndex200Response**](../Model/StoresIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storesUpdate()`

```php
storesUpdate($promotion_id, $stores_create_request): \IdpluggerPromotion\Model\StoresUpdate201Response
```

Cadastra ou atualiza lojas na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\StoresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$stores_create_request = new \IdpluggerPromotion\Model\StoresCreateRequest(); // \IdpluggerPromotion\Model\StoresCreateRequest

try {
    $result = $apiInstance->storesUpdate($promotion_id, $stores_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoresApi->storesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **stores_create_request** | [**\IdpluggerPromotion\Model\StoresCreateRequest**](../Model/StoresCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\StoresUpdate201Response**](../Model/StoresUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
