# IdPluggerPromotion\FAQApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionFaqCreate()**](FAQApi.md#promotionFaqCreate) | **POST** /v3/promotion/{promotion_id}/cms/faq | Cadastra perguntas frequentes na promoção |
| [**promotionFaqDelete()**](FAQApi.md#promotionFaqDelete) | **DELETE** /v3/promotion/{promotion_id}/cms/faq | Esclui perguntas frequentes na promoção |
| [**promotionFaqIndex()**](FAQApi.md#promotionFaqIndex) | **GET** /v3/promotion/{promotion_id}/cms/faq | Lista as perguntas frequentes cadastradas na promoção |
| [**promotionFaqUpdate()**](FAQApi.md#promotionFaqUpdate) | **PATCH** /v3/promotion/{promotion_id}/cms/faq | Cadastra ou atualiza perguntas frequentes na promoção |


## `promotionFaqCreate()`

```php
promotionFaqCreate($promotion_id, $promotion_faq_create_request_inner): \IdPluggerPromotion\Model\PromotionFaqCreate200Response
```

Cadastra perguntas frequentes na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_faq_create_request_inner = array(new \IdPluggerPromotion\Model\PromotionFaqCreateRequestInner()); // \IdPluggerPromotion\Model\PromotionFaqCreateRequestInner[]

try {
    $result = $apiInstance->promotionFaqCreate($promotion_id, $promotion_faq_create_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->promotionFaqCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_faq_create_request_inner** | [**\IdPluggerPromotion\Model\PromotionFaqCreateRequestInner[]**](../Model/PromotionFaqCreateRequestInner.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionFaqCreate200Response**](../Model/PromotionFaqCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionFaqDelete()`

```php
promotionFaqDelete($promotion_id, $answer): \IdPluggerPromotion\Model\PromotionFaqDelete200Response
```

Esclui perguntas frequentes na promoção

A exclusão é feita caso haja uma pergunta frequente com a mesma question enviada.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$answer = 'answer_example'; // string | Pergunta da questão a ser excluída

try {
    $result = $apiInstance->promotionFaqDelete($promotion_id, $answer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->promotionFaqDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **answer** | **string**| Pergunta da questão a ser excluída | |

### Return type

[**\IdPluggerPromotion\Model\PromotionFaqDelete200Response**](../Model/PromotionFaqDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionFaqIndex()`

```php
promotionFaqIndex($promotion_id, $question, $answer): \IdPluggerPromotion\Model\PromotionFaqIndex200Response
```

Lista as perguntas frequentes cadastradas na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$question = O que será sorteado?; // string | Pesquisa perguntas frequentes através da questão
$answer = Será sorteado um smartphone; // string | Pesquisa perguntas frequentes através da resposta

try {
    $result = $apiInstance->promotionFaqIndex($promotion_id, $question, $answer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->promotionFaqIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **question** | **string**| Pesquisa perguntas frequentes através da questão | [optional] |
| **answer** | **string**| Pesquisa perguntas frequentes através da resposta | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionFaqIndex200Response**](../Model/PromotionFaqIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionFaqUpdate()`

```php
promotionFaqUpdate($promotion_id, $promotion_faq_create_request_inner): \IdPluggerPromotion\Model\PromotionFaqUpdate200Response
```

Cadastra ou atualiza perguntas frequentes na promoção

A atualização é feita caso haja uma pergunta frequente com a mesma question enviada para cadastro.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_faq_create_request_inner = array(new \IdPluggerPromotion\Model\PromotionFaqCreateRequestInner()); // \IdPluggerPromotion\Model\PromotionFaqCreateRequestInner[]

try {
    $result = $apiInstance->promotionFaqUpdate($promotion_id, $promotion_faq_create_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->promotionFaqUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_faq_create_request_inner** | [**\IdPluggerPromotion\Model\PromotionFaqCreateRequestInner[]**](../Model/PromotionFaqCreateRequestInner.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionFaqUpdate200Response**](../Model/PromotionFaqUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
