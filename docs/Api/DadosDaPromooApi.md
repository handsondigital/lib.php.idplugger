# IdPluggerPromotion\DadosDaPromooApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionConfigsIndex()**](DadosDaPromooApi.md#promotionConfigsIndex) | **GET** /v3/promotion/{promotion_id} | Retorna dados da promoção |


## `promotionConfigsIndex()`

```php
promotionConfigsIndex($promotion_id): \IdPluggerPromotion\Model\PromotionConfigsIndex200Response
```

Retorna dados da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\DadosDaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção

try {
    $result = $apiInstance->promotionConfigsIndex($promotion_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DadosDaPromooApi->promotionConfigsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |

### Return type

[**\IdPluggerPromotion\Model\PromotionConfigsIndex200Response**](../Model/PromotionConfigsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
