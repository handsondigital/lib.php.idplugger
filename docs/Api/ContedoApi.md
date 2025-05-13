# IdPluggerPromotion\ContedoApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionContentCreate()**](ContedoApi.md#promotionContentCreate) | **POST** /v3/promotion/{promotion_id}/cms/content | Cria um novo conteúdo para a promoção |
| [**promotionContentIndex()**](ContedoApi.md#promotionContentIndex) | **GET** /v3/promotion/{promotion_id}/cms/content | Dados referentes aos conteúdos (que não são artigos de blog) da promoção |


## `promotionContentCreate()`

```php
promotionContentCreate($promotion_id, $content): \IdPluggerPromotion\Model\PromotionContentCreate200Response
```

Cria um novo conteúdo para a promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\ContedoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$content = new \IdPluggerPromotion\Model\Content(); // \IdPluggerPromotion\Model\Content

try {
    $result = $apiInstance->promotionContentCreate($promotion_id, $content);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContedoApi->promotionContentCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **content** | [**\IdPluggerPromotion\Model\Content**](../Model/Content.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionContentCreate200Response**](../Model/PromotionContentCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionContentIndex()`

```php
promotionContentIndex($promotion_id, $_fields, $key, $group, $type): \IdPluggerPromotion\Model\PromotionContentIndex200Response
```

Dados referentes aos conteúdos (que não são artigos de blog) da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\ContedoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,key,value,order,type,group; // string | Campos a serem retornados pela API
$key = como_participar; // string | Pesquisa pela chave principal do conteúdo
$group = como_participar; // string | Pesquisa pela chave do grupo do conteúdo
$type = json; // string | Pesquisa pelo tipo do conteúdo

try {
    $result = $apiInstance->promotionContentIndex($promotion_id, $_fields, $key, $group, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContedoApi->promotionContentIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados pela API | [optional] |
| **key** | **string**| Pesquisa pela chave principal do conteúdo | [optional] |
| **group** | **string**| Pesquisa pela chave do grupo do conteúdo | [optional] |
| **type** | **string**| Pesquisa pelo tipo do conteúdo | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionContentIndex200Response**](../Model/PromotionContentIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
