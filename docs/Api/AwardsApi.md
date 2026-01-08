# IdpluggerPromotion\AwardsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**awardsCreate()**](AwardsApi.md#awardsCreate) | **POST** /v3/promotion/{promotion_id}/awards | Cadastra um prêmio na promoção |
| [**awardsDelete()**](AwardsApi.md#awardsDelete) | **DELETE** /v3/promotion/{promotion_id}/awards/{id} | Deleta um prêmio da promoção |
| [**awardsIndex()**](AwardsApi.md#awardsIndex) | **GET** /v3/promotion/{promotion_id}/awards | Pesquisa por prêmios na promoção |
| [**awardsUpdate()**](AwardsApi.md#awardsUpdate) | **PATCH** /v3/promotion/{promotion_id}/awards | Cadastra ou atualiza um prêmio na promoção |


## `awardsCreate()`

```php
awardsCreate($promotion_id, $award): \IdpluggerPromotion\Model\AwardsCreate200Response
```

Cadastra um prêmio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AwardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$award = array(new \IdpluggerPromotion\Model\Award()); // \IdpluggerPromotion\Model\Award[]

try {
    $result = $apiInstance->awardsCreate($promotion_id, $award);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AwardsApi->awardsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **award** | [**\IdpluggerPromotion\Model\Award[]**](../Model/Award.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\AwardsCreate200Response**](../Model/AwardsCreate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `awardsDelete()`

```php
awardsDelete($promotion_id, $id): \IdpluggerPromotion\Model\AwardsDelete200Response
```

Deleta um prêmio da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AwardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 'id_example'; // string | ID do prêmio

try {
    $result = $apiInstance->awardsDelete($promotion_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AwardsApi->awardsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **string**| ID do prêmio | |

### Return type

[**\IdpluggerPromotion\Model\AwardsDelete200Response**](../Model/AwardsDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `awardsIndex()`

```php
awardsIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $raffle_id, $raffle_type): \IdpluggerPromotion\Model\AwardsIndex200Response
```

Pesquisa por prêmios na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AwardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$_fields = id,name,raffle_type; // string | Campos a serem retornados
$_include = raffles,lotterys,awardeds; // string | Dados relacionados a serem retornados
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa
$id = 1; // string | Id do prêmio
$raffle_id = 1; // string | Id do sorteio
$raffle_type = normal; // string | Tipo do sorteio

try {
    $result = $apiInstance->awardsIndex($promotion_id, $_fields, $_include, $page, $_per_page, $id, $raffle_id, $raffle_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AwardsApi->awardsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **_fields** | **string**| Campos a serem retornados | [optional] |
| **_include** | **string**| Dados relacionados a serem retornados | [optional] |
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |
| **id** | **string**| Id do prêmio | [optional] |
| **raffle_id** | **string**| Id do sorteio | [optional] |
| **raffle_type** | **string**| Tipo do sorteio | [optional] |

### Return type

[**\IdpluggerPromotion\Model\AwardsIndex200Response**](../Model/AwardsIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `awardsUpdate()`

```php
awardsUpdate($promotion_id, $award): \IdpluggerPromotion\Model\AwardsUpdate200Response
```

Cadastra ou atualiza um prêmio na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\AwardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$award = array(new \IdpluggerPromotion\Model\Award()); // \IdpluggerPromotion\Model\Award[]

try {
    $result = $apiInstance->awardsUpdate($promotion_id, $award);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AwardsApi->awardsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **award** | [**\IdpluggerPromotion\Model\Award[]**](../Model/Award.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\AwardsUpdate200Response**](../Model/AwardsUpdate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
