# IdpluggerPromotion\ArticlesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**articlesCreate()**](ArticlesApi.md#articlesCreate) | **POST** /v3/promotion/{promotion_id}/cms/articles | Cadastra publicações na promoção |
| [**articlesDelete()**](ArticlesApi.md#articlesDelete) | **DELETE** /v3/promotion/{promotion_id}/cms/articles/{id} | Exclui uma publicação da promoção |
| [**articlesIndex()**](ArticlesApi.md#articlesIndex) | **GET** /v3/promotion/{promotion_id}/cms/articles | Lista as publicações cadastradas na promoção |
| [**articlesUpdate()**](ArticlesApi.md#articlesUpdate) | **PATCH** /v3/promotion/{promotion_id}/cms/articles | Cadastra ou atualiza publicações na promoção |


## `articlesCreate()`

```php
articlesCreate($promotion_id, $article): \IdpluggerPromotion\Model\ArticlesCreate200Response
```

Cadastra publicações na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ArticlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$article = array(new \IdpluggerPromotion\Model\Article()); // \IdpluggerPromotion\Model\Article[]

try {
    $result = $apiInstance->articlesCreate($promotion_id, $article);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articlesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **article** | [**\IdpluggerPromotion\Model\Article[]**](../Model/Article.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ArticlesCreate200Response**](../Model/ArticlesCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `articlesDelete()`

```php
articlesDelete($promotion_id, $id): \IdpluggerPromotion\Model\ArticlesDelete200Response
```

Exclui uma publicação da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ArticlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 'id_example'; // string | ID da publicação

try {
    $result = $apiInstance->articlesDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articlesDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **string**| ID da publicação | |

### Return type

[**\IdpluggerPromotion\Model\ArticlesDelete200Response**](../Model/ArticlesDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `articlesIndex()`

```php
articlesIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $title, $_keyword, $date, $created_at, $updated_at): \IdpluggerPromotion\Model\ArticlesIndex200Response
```

Lista as publicações cadastradas na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ArticlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,title,image,author_id,created_at; // string | Informa quais campos devem ser retornados na pesquisa pela API
$_include = customFields; // string | Informa se os dados do autor da publicação também deve ser retornado na pesquisa pela API
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de publicações por página na pesquisa
$id = 1,3,5; // string | Pesquisa publicações cadastradas na promoção pelo id das mesmas
$title = comércio eletrônico; // string | Pesquisa publicações cadastradas na promoção com título que contenha o texto pesquisado
$_keyword = sorteios são demais; // string | Pesquisa publicações cadastradas na promoção com texto que contenha o texto pesquisado
$date = 2021/01/01 00:00:00 AND 2021/01/31 23:59:59 ; // string | Pesquisa publicações cadastradas na promoção com data de publicação entre as datas informadas
$created_at = 2021/01/01 00:00:00 AND 2021/01/31 23:59:59 ; // string | Pesquisa publicações cadastradas na promoção entre as datas informadas
$updated_at = 2021/01/01 00:00:00 AND 2021/01/31 23:59:59 ; // string | Pesquisa publicações cadastradas na promoção atualizadas entre as datas informadas

try {
    $result = $apiInstance->articlesIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $title, $_keyword, $date, $created_at, $updated_at);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articlesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Informa quais campos devem ser retornados na pesquisa pela API | [optional] |
| **_include** | **string**| Informa se os dados do autor da publicação também deve ser retornado na pesquisa pela API | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de publicações por página na pesquisa | [optional] |
| **id** | **string**| Pesquisa publicações cadastradas na promoção pelo id das mesmas | [optional] |
| **title** | **string**| Pesquisa publicações cadastradas na promoção com título que contenha o texto pesquisado | [optional] |
| **_keyword** | **string**| Pesquisa publicações cadastradas na promoção com texto que contenha o texto pesquisado | [optional] |
| **date** | **string**| Pesquisa publicações cadastradas na promoção com data de publicação entre as datas informadas | [optional] |
| **created_at** | **string**| Pesquisa publicações cadastradas na promoção entre as datas informadas | [optional] |
| **updated_at** | **string**| Pesquisa publicações cadastradas na promoção atualizadas entre as datas informadas | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ArticlesIndex200Response**](../Model/ArticlesIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `articlesUpdate()`

```php
articlesUpdate($promotion_id, $article): \IdpluggerPromotion\Model\ArticlesUpdate200Response
```

Cadastra ou atualiza publicações na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\ArticlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$article = array(new \IdpluggerPromotion\Model\Article()); // \IdpluggerPromotion\Model\Article[]

try {
    $result = $apiInstance->articlesUpdate($promotion_id, $article);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articlesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **article** | [**\IdpluggerPromotion\Model\Article[]**](../Model/Article.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ArticlesUpdate200Response**](../Model/ArticlesUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
