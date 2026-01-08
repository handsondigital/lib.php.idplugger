# IdpluggerPromotion\FAQApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**faqCreate()**](FAQApi.md#faqCreate) | **POST** /v3/promotion/{promotion_id}/cms/faq | Cadastra perguntas frequentes na promoção |
| [**faqDelete()**](FAQApi.md#faqDelete) | **DELETE** /v3/promotion/{promotion_id}/cms/faq | Esclui perguntas frequentes na promoção |
| [**faqIndex()**](FAQApi.md#faqIndex) | **GET** /v3/promotion/{promotion_id}/cms/faq | Lista as perguntas frequentes cadastradas na promoção |
| [**faqUpdate()**](FAQApi.md#faqUpdate) | **PATCH** /v3/promotion/{promotion_id}/cms/faq | Cadastra ou atualiza perguntas frequentes na promoção |


## `faqCreate()`

```php
faqCreate($promotion_id, $faq_create_request_inner): \IdpluggerPromotion\Model\FaqCreate200Response
```

Cadastra perguntas frequentes na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$faq_create_request_inner = array(new \IdpluggerPromotion\Model\FaqCreateRequestInner()); // \IdpluggerPromotion\Model\FaqCreateRequestInner[]

try {
    $result = $apiInstance->faqCreate($promotion_id, $faq_create_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->faqCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **faq_create_request_inner** | [**\IdpluggerPromotion\Model\FaqCreateRequestInner[]**](../Model/FaqCreateRequestInner.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\FaqCreate200Response**](../Model/FaqCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `faqDelete()`

```php
faqDelete($promotion_id, $answer): \IdpluggerPromotion\Model\FaqDelete200Response
```

Esclui perguntas frequentes na promoção

A exclusão é feita caso haja uma pergunta frequente com a mesma question enviada.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$answer = 'answer_example'; // string | Pergunta da questão a ser excluída

try {
    $result = $apiInstance->faqDelete($promotion_id, $answer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->faqDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **answer** | **string**| Pergunta da questão a ser excluída | |

### Return type

[**\IdpluggerPromotion\Model\FaqDelete200Response**](../Model/FaqDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `faqIndex()`

```php
faqIndex($promotion_id, $page, $_per_page, $question, $answer): \IdpluggerPromotion\Model\FaqIndex200Response
```

Lista as perguntas frequentes cadastradas na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$question = O que será sorteado?; // string | Pesquisa perguntas frequentes através da questão
$answer = Será sorteado um smartphone; // string | Pesquisa perguntas frequentes através da resposta

try {
    $result = $apiInstance->faqIndex($promotion_id, $page, $_per_page, $question, $answer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->faqIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **question** | **string**| Pesquisa perguntas frequentes através da questão | [optional] |
| **answer** | **string**| Pesquisa perguntas frequentes através da resposta | [optional] |

### Return type

[**\IdpluggerPromotion\Model\FaqIndex200Response**](../Model/FaqIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `faqUpdate()`

```php
faqUpdate($promotion_id, $faq_create_request_inner): \IdpluggerPromotion\Model\FaqUpdate200Response
```

Cadastra ou atualiza perguntas frequentes na promoção

A atualização é feita caso haja uma pergunta frequente com a mesma question enviada para cadastro.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\FAQApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$faq_create_request_inner = array(new \IdpluggerPromotion\Model\FaqCreateRequestInner()); // \IdpluggerPromotion\Model\FaqCreateRequestInner[]

try {
    $result = $apiInstance->faqUpdate($promotion_id, $faq_create_request_inner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAQApi->faqUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **faq_create_request_inner** | [**\IdpluggerPromotion\Model\FaqCreateRequestInner[]**](../Model/FaqCreateRequestInner.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\FaqUpdate200Response**](../Model/FaqUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
