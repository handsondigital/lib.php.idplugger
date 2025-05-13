# IdpluggerPromotion\BrandingApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**brandingIndex()**](BrandingApi.md#brandingIndex) | **GET** /v3/promotion/{promotion_id}/cms/branding | Dados referentes a identidade visual da marca da promoção |
| [**brandingUpdate()**](BrandingApi.md#brandingUpdate) | **POST** /v3/promotion/{promotion_id}/cms/branding | Altera os dados referentes a identidade visual da marca da promoção |


## `brandingIndex()`

```php
brandingIndex($promotion_id, $_fields): \IdpluggerPromotion\Model\BrandingIndex200Response
```

Dados referentes a identidade visual da marca da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,assunto,content; // string | Campos a serem retornados pela API

try {
    $result = $apiInstance->brandingIndex($promotion_id, $_fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->brandingIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados pela API | [optional] |

### Return type

[**\IdpluggerPromotion\Model\BrandingIndex200Response**](../Model/BrandingIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `brandingUpdate()`

```php
brandingUpdate($promotion_id, $branding): \IdpluggerPromotion\Model\BrandingUpdate200Response
```

Altera os dados referentes a identidade visual da marca da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$branding = new \IdpluggerPromotion\Model\Branding(); // \IdpluggerPromotion\Model\Branding

try {
    $result = $apiInstance->brandingUpdate($promotion_id, $branding);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->brandingUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **branding** | [**\IdpluggerPromotion\Model\Branding**](../Model/Branding.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\BrandingUpdate200Response**](../Model/BrandingUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
