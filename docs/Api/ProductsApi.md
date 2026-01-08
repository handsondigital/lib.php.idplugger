# IdpluggerPromotion\ProductsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**productsCreate()**](ProductsApi.md#productsCreate) | **POST** /v3/promotion/{promotion_id}/products | Cadastra um produto na promoção |
| [**productsDelete()**](ProductsApi.md#productsDelete) | **DELETE** /v3/promotion/{promotion_id}/products/{product_id} | Exclui um produto cadastrado na promoção |
| [**productsIndex()**](ProductsApi.md#productsIndex) | **GET** /v3/promotion/{promotion_id}/products | Busca por produtos cadastrados na promoção |
| [**productsUpdate()**](ProductsApi.md#productsUpdate) | **PATCH** /v3/promotion/{promotion_id}/products | Cadastra ou atualiza produtos na promoção |


## `productsCreate()`

```php
productsCreate($promotion_id, $products_create_request): \IdpluggerPromotion\Model\ProductsCreate200Response
```

Cadastra um produto na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$products_create_request = new \IdpluggerPromotion\Model\ProductsCreateRequest(); // \IdpluggerPromotion\Model\ProductsCreateRequest

try {
    $result = $apiInstance->productsCreate($promotion_id, $products_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **products_create_request** | [**\IdpluggerPromotion\Model\ProductsCreateRequest**](../Model/ProductsCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ProductsCreate200Response**](../Model/ProductsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsDelete()`

```php
productsDelete($promotion_id, $product_id): \IdpluggerPromotion\Model\ProductsDelete200Response
```

Exclui um produto cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$product_id = 'product_id_example'; // string | ID do produto

try {
    $result = $apiInstance->productsDelete($promotion_id, $product_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **product_id** | **string**| ID do produto | |

### Return type

[**\IdpluggerPromotion\Model\ProductsDelete200Response**](../Model/ProductsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsIndex()`

```php
productsIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $serial_number): \IdpluggerPromotion\Model\ProductsIndex200Response
```

Busca por produtos cadastrados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ProductsApi(
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
$id = 'id_example'; // string | Id do produto
$serial_number = 'serial_number_example'; // string | Número serial do produto

try {
    $result = $apiInstance->productsIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $serial_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsIndex: ', $e->getMessage(), PHP_EOL;
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
| **id** | **string**| Id do produto | [optional] |
| **serial_number** | **string**| Número serial do produto | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ProductsIndex200Response**](../Model/ProductsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsUpdate()`

```php
productsUpdate($promotion_id, $products_create_request): \IdpluggerPromotion\Model\ProductsUpdate201Response
```

Cadastra ou atualiza produtos na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$products_create_request = new \IdpluggerPromotion\Model\ProductsCreateRequest(); // \IdpluggerPromotion\Model\ProductsCreateRequest

try {
    $result = $apiInstance->productsUpdate($promotion_id, $products_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **products_create_request** | [**\IdpluggerPromotion\Model\ProductsCreateRequest**](../Model/ProductsCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ProductsUpdate201Response**](../Model/ProductsUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
