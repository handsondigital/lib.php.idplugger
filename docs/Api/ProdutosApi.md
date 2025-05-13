# IdPluggerPromotion\ProdutosApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionProductsCreate()**](ProdutosApi.md#promotionProductsCreate) | **POST** /v3/promotion/{promotion_id}/products | Cadastra um produto na promoção |
| [**promotionProductsDelete()**](ProdutosApi.md#promotionProductsDelete) | **DELETE** /v3/promotion/{promotion_id}/products/{product_id} | Exclui um produto cadastrado na promoção |
| [**promotionProductsIndex()**](ProdutosApi.md#promotionProductsIndex) | **GET** /v3/promotion/{promotion_id}/products | Busca por produtos cadastrados na promoção |
| [**promotionProductsUpdate()**](ProdutosApi.md#promotionProductsUpdate) | **PATCH** /v3/promotion/{promotion_id}/products | Cadastra ou atualiza produtos na promoção |
| [**promotionStoresDelete()**](ProdutosApi.md#promotionStoresDelete) | **DELETE** /v3/promotion/{promotion_id}/stores/{store_id} | Exclui um produto cadastrado na promoção |


## `promotionProductsCreate()`

```php
promotionProductsCreate($promotion_id, $promotion_products_create_request): \IdPluggerPromotion\Model\PromotionProductsCreate200Response
```

Cadastra um produto na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\ProdutosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_products_create_request = new \IdPluggerPromotion\Model\PromotionProductsCreateRequest(); // \IdPluggerPromotion\Model\PromotionProductsCreateRequest

try {
    $result = $apiInstance->promotionProductsCreate($promotion_id, $promotion_products_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProdutosApi->promotionProductsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_products_create_request** | [**\IdPluggerPromotion\Model\PromotionProductsCreateRequest**](../Model/PromotionProductsCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionProductsCreate200Response**](../Model/PromotionProductsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionProductsDelete()`

```php
promotionProductsDelete($promotion_id, $product_id): \IdPluggerPromotion\Model\PromotionProductsDelete200Response
```

Exclui um produto cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\ProdutosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$product_id = 'product_id_example'; // string | ID do produto

try {
    $result = $apiInstance->promotionProductsDelete($promotion_id, $product_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProdutosApi->promotionProductsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **product_id** | **string**| ID do produto | |

### Return type

[**\IdPluggerPromotion\Model\PromotionProductsDelete200Response**](../Model/PromotionProductsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionProductsIndex()`

```php
promotionProductsIndex($promotion_id, $_fields, $_include, $id, $serial_number): \IdPluggerPromotion\Model\PromotionProductsIndex200Response
```

Busca por produtos cadastrados na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\ProdutosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = ["id"]; // string | Campos a serem retornados
$_include = ["coupons"]; // string | Associações a serem retornadas
$id = 'id_example'; // string | Id do produto
$serial_number = 'serial_number_example'; // string | Número serial do produto

try {
    $result = $apiInstance->promotionProductsIndex($promotion_id, $_fields, $_include, $id, $serial_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProdutosApi->promotionProductsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Associações a serem retornadas | [optional] |
| **id** | **string**| Id do produto | [optional] |
| **serial_number** | **string**| Número serial do produto | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionProductsIndex200Response**](../Model/PromotionProductsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionProductsUpdate()`

```php
promotionProductsUpdate($promotion_id, $promotion_products_create_request): \IdPluggerPromotion\Model\PromotionProductsUpdate201Response
```

Cadastra ou atualiza produtos na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\ProdutosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_products_create_request = new \IdPluggerPromotion\Model\PromotionProductsCreateRequest(); // \IdPluggerPromotion\Model\PromotionProductsCreateRequest

try {
    $result = $apiInstance->promotionProductsUpdate($promotion_id, $promotion_products_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProdutosApi->promotionProductsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_products_create_request** | [**\IdPluggerPromotion\Model\PromotionProductsCreateRequest**](../Model/PromotionProductsCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionProductsUpdate201Response**](../Model/PromotionProductsUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionStoresDelete()`

```php
promotionStoresDelete($promotion_id, $store_id): \IdPluggerPromotion\Model\PromotionStoresDelete200Response
```

Exclui um produto cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\ProdutosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$store_id = 'store_id_example'; // string | ID da loja

try {
    $result = $apiInstance->promotionStoresDelete($promotion_id, $store_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProdutosApi->promotionStoresDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **store_id** | **string**| ID da loja | |

### Return type

[**\IdPluggerPromotion\Model\PromotionStoresDelete200Response**](../Model/PromotionStoresDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
