# IdpluggerPromotion\DocumentRulesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**documentRulesIndex()**](DocumentRulesApi.md#documentRulesIndex) | **GET** /v3/promotion/{promotion_id}/cms/document_rules | Termos de uso, regulamentos e política de privacidade da promoção |
| [**documentRulesRegulationDelete()**](DocumentRulesApi.md#documentRulesRegulationDelete) | **DELETE** /v3/promotion/{promotion_id}/cms/document_rules/regulation/{regulation_id} | Exclui um regulamento da promoção |
| [**documentRulesUpdate()**](DocumentRulesApi.md#documentRulesUpdate) | **POST** /v3/promotion/{promotion_id}/cms/document_rules | Atualiza os termos de uso e regulamento da promoção |


## `documentRulesIndex()`

```php
documentRulesIndex($promotion_id): \IdpluggerPromotion\Model\DocumentRulesIndex200Response
```

Termos de uso, regulamentos e política de privacidade da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\DocumentRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção

try {
    $result = $apiInstance->documentRulesIndex($promotion_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentRulesApi->documentRulesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |

### Return type

[**\IdpluggerPromotion\Model\DocumentRulesIndex200Response**](../Model/DocumentRulesIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `documentRulesRegulationDelete()`

```php
documentRulesRegulationDelete($promotion_id, $regulation_id): \IdpluggerPromotion\Model\DocumentRulesRegulationDelete200Response
```

Exclui um regulamento da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\DocumentRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$regulation_id = 'regulation_id_example'; // string | ID do regulamento

try {
    $result = $apiInstance->documentRulesRegulationDelete($promotion_id, $regulation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentRulesApi->documentRulesRegulationDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **regulation_id** | **string**| ID do regulamento | |

### Return type

[**\IdpluggerPromotion\Model\DocumentRulesRegulationDelete200Response**](../Model/DocumentRulesRegulationDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `documentRulesUpdate()`

```php
documentRulesUpdate($promotion_id, $document_rules_update_request): \IdpluggerPromotion\Model\DocumentRulesUpdate200Response
```

Atualiza os termos de uso e regulamento da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\DocumentRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$document_rules_update_request = new \IdpluggerPromotion\Model\DocumentRulesUpdateRequest(); // \IdpluggerPromotion\Model\DocumentRulesUpdateRequest

try {
    $result = $apiInstance->documentRulesUpdate($promotion_id, $document_rules_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentRulesApi->documentRulesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **document_rules_update_request** | [**\IdpluggerPromotion\Model\DocumentRulesUpdateRequest**](../Model/DocumentRulesUpdateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\DocumentRulesUpdate200Response**](../Model/DocumentRulesUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
