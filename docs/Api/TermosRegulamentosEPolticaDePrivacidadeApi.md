# IdPluggerPromotion\TermosRegulamentosEPolticaDePrivacidadeApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionDocumentRulesIndex()**](TermosRegulamentosEPolticaDePrivacidadeApi.md#promotionDocumentRulesIndex) | **GET** /v3/promotion/{promotion_id}/cms/document_rules | Termos de uso, regulamentos e política de privacidade da promoção |
| [**promotionDocumentRulesRegulationDelete()**](TermosRegulamentosEPolticaDePrivacidadeApi.md#promotionDocumentRulesRegulationDelete) | **DELETE** /v3/promotion/{promotion_id}/cms/document_rules/regulation/{regulation_id} | Exclui um regulamento da promoção |
| [**promotionDocumentRulesUpdate()**](TermosRegulamentosEPolticaDePrivacidadeApi.md#promotionDocumentRulesUpdate) | **POST** /v3/promotion/{promotion_id}/cms/document_rules | Atualiza os termos de uso e regulamento da promoção |


## `promotionDocumentRulesIndex()`

```php
promotionDocumentRulesIndex($promotion_id): \IdPluggerPromotion\Model\PromotionDocumentRulesIndex200Response
```

Termos de uso, regulamentos e política de privacidade da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\TermosRegulamentosEPolticaDePrivacidadeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção

try {
    $result = $apiInstance->promotionDocumentRulesIndex($promotion_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermosRegulamentosEPolticaDePrivacidadeApi->promotionDocumentRulesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |

### Return type

[**\IdPluggerPromotion\Model\PromotionDocumentRulesIndex200Response**](../Model/PromotionDocumentRulesIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionDocumentRulesRegulationDelete()`

```php
promotionDocumentRulesRegulationDelete($promotion_id, $regulation_id): \IdPluggerPromotion\Model\PromotionDocumentRulesRegulationDelete200Response
```

Exclui um regulamento da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\TermosRegulamentosEPolticaDePrivacidadeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$regulation_id = 'regulation_id_example'; // string | ID do regulamento

try {
    $result = $apiInstance->promotionDocumentRulesRegulationDelete($promotion_id, $regulation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermosRegulamentosEPolticaDePrivacidadeApi->promotionDocumentRulesRegulationDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **regulation_id** | **string**| ID do regulamento | |

### Return type

[**\IdPluggerPromotion\Model\PromotionDocumentRulesRegulationDelete200Response**](../Model/PromotionDocumentRulesRegulationDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionDocumentRulesUpdate()`

```php
promotionDocumentRulesUpdate($promotion_id, $promotion_document_rules_update_request): \IdPluggerPromotion\Model\PromotionDocumentRulesUpdate200Response
```

Atualiza os termos de uso e regulamento da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\TermosRegulamentosEPolticaDePrivacidadeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_document_rules_update_request = new \IdPluggerPromotion\Model\PromotionDocumentRulesUpdateRequest(); // \IdPluggerPromotion\Model\PromotionDocumentRulesUpdateRequest

try {
    $result = $apiInstance->promotionDocumentRulesUpdate($promotion_id, $promotion_document_rules_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TermosRegulamentosEPolticaDePrivacidadeApi->promotionDocumentRulesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_document_rules_update_request** | [**\IdPluggerPromotion\Model\PromotionDocumentRulesUpdateRequest**](../Model/PromotionDocumentRulesUpdateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionDocumentRulesUpdate200Response**](../Model/PromotionDocumentRulesUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
