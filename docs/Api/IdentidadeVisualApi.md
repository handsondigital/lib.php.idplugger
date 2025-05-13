# IdPluggerPromotion\IdentidadeVisualApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionBrandingIndex()**](IdentidadeVisualApi.md#promotionBrandingIndex) | **GET** /v3/promotion/{promotion_id}/cms/branding | Dados referentes a identidade visual da marca da promoção |
| [**promotionBrandingUpdate()**](IdentidadeVisualApi.md#promotionBrandingUpdate) | **POST** /v3/promotion/{promotion_id}/cms/branding | Altera os dados referentes a identidade visual da marca da promoção |


## `promotionBrandingIndex()`

```php
promotionBrandingIndex($promotion_id, $_fields): \IdPluggerPromotion\Model\PromotionBrandingIndex200Response
```

Dados referentes a identidade visual da marca da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\IdentidadeVisualApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,assunto,content; // string | Campos a serem retornados pela API

try {
    $result = $apiInstance->promotionBrandingIndex($promotion_id, $_fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentidadeVisualApi->promotionBrandingIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados pela API | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionBrandingIndex200Response**](../Model/PromotionBrandingIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionBrandingUpdate()`

```php
promotionBrandingUpdate($promotion_id, $branding): \IdPluggerPromotion\Model\PromotionBrandingUpdate200Response
```

Altera os dados referentes a identidade visual da marca da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\IdentidadeVisualApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$branding = new \IdPluggerPromotion\Model\Branding(); // \IdPluggerPromotion\Model\Branding

try {
    $result = $apiInstance->promotionBrandingUpdate($promotion_id, $branding);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentidadeVisualApi->promotionBrandingUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **branding** | [**\IdPluggerPromotion\Model\Branding**](../Model/Branding.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionBrandingUpdate200Response**](../Model/PromotionBrandingUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
