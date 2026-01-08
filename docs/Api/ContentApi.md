# IdpluggerPromotion\ContentApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contentCreate()**](ContentApi.md#contentCreate) | **POST** /v3/promotion/{promotion_id}/cms/content | Cria um novo conteúdo para a promoção |
| [**contentIndex()**](ContentApi.md#contentIndex) | **GET** /v3/promotion/{promotion_id}/cms/content | Dados referentes aos conteúdos (que não são artigos de blog) da promoção |


## `contentCreate()`

```php
contentCreate($promotion_id, $content): \IdpluggerPromotion\Model\ContentCreate200Response
```

Cria um novo conteúdo para a promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$content = new \IdpluggerPromotion\Model\Content(); // \IdpluggerPromotion\Model\Content

try {
    $result = $apiInstance->contentCreate($promotion_id, $content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->contentCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **content** | [**\IdpluggerPromotion\Model\Content**](../Model/Content.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ContentCreate200Response**](../Model/ContentCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `contentIndex()`

```php
contentIndex($promotion_id, $_fields, $page, $_per_page, $key, $group, $type): \IdpluggerPromotion\Model\ContentIndex200Response
```

Dados referentes aos conteúdos (que não são artigos de blog) da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,key,value,order,type,group; // string | Campos a serem retornados pela API
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$key = como_participar; // string | Pesquisa pela chave principal do conteúdo
$group = como_participar; // string | Pesquisa pela chave do grupo do conteúdo
$type = json; // string | Pesquisa pelo tipo do conteúdo

try {
    $result = $apiInstance->contentIndex($promotion_id, $_fields, $page, $_per_page, $key, $group, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentApi->contentIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados pela API | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **key** | **string**| Pesquisa pela chave principal do conteúdo | [optional] |
| **group** | **string**| Pesquisa pela chave do grupo do conteúdo | [optional] |
| **type** | **string**| Pesquisa pelo tipo do conteúdo | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ContentIndex200Response**](../Model/ContentIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
