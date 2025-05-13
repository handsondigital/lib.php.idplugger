# IdPluggerPromotion\UsuriosNaPromooApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**promotionUsersCreate()**](UsuriosNaPromooApi.md#promotionUsersCreate) | **POST** /v3/promotion/{promotion_id}/users | Cadastra um usuário na promoção |
| [**promotionUsersDelete()**](UsuriosNaPromooApi.md#promotionUsersDelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id} | Exclui um usuário da promoção |
| [**promotionUsersIndex()**](UsuriosNaPromooApi.md#promotionUsersIndex) | **GET** /v3/promotion/{promotion_id}/users | Busca por um usuário cadastrado na promoção |
| [**promotionUsersUpdate()**](UsuriosNaPromooApi.md#promotionUsersUpdate) | **PATCH** /v3/promotion/{promotion_id}/users | Cadastra ou atualiza um usuário na promoção |
| [**promotionUsersWebhook()**](UsuriosNaPromooApi.md#promotionUsersWebhook) | **POST** /webhook-do-usuario | Webhook de resposta ao registro de usuário |


## `promotionUsersCreate()`

```php
promotionUsersCreate($promotion_id, $promotion_users_create_request): \IdPluggerPromotion\Model\PromotionUsersCreate201Response
```

Cadastra um usuário na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\UsuriosNaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_users_create_request = new \IdPluggerPromotion\Model\PromotionUsersCreateRequest(); // \IdPluggerPromotion\Model\PromotionUsersCreateRequest

try {
    $result = $apiInstance->promotionUsersCreate($promotion_id, $promotion_users_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsuriosNaPromooApi->promotionUsersCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_users_create_request** | [**\IdPluggerPromotion\Model\PromotionUsersCreateRequest**](../Model/PromotionUsersCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionUsersCreate201Response**](../Model/PromotionUsersCreate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionUsersDelete()`

```php
promotionUsersDelete($promotion_id, $user_id): \IdPluggerPromotion\Model\PromotionUsersDelete200Response
```

Exclui um usuário da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\UsuriosNaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário

try {
    $result = $apiInstance->promotionUsersDelete($promotion_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsuriosNaPromooApi->promotionUsersDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |

### Return type

[**\IdPluggerPromotion\Model\PromotionUsersDelete200Response**](../Model/PromotionUsersDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionUsersIndex()`

```php
promotionUsersIndex($promotion_id, $id, $external_id, $username, $email, $cpf, $_include, $_fields): \IdPluggerPromotion\Model\PromotionUsersIndex200Response
```

Busca por um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\UsuriosNaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$id = 56; // int | ID do usuário
$external_id = 'external_id_example'; // string | ID externo do usuário
$username = 'username_example'; // string | username do usuário
$email = 'email_example'; // string | email do usuário
$cpf = 'cpf_example'; // string | CPF do usuário
$_include = custom_data,coupons,lucky_numbers; // string | Dados relacionados a serem retornados
$_fields = id,username,email,name,birth,cpf,rg,cep,address,number,complement,neighborhood,city,state,phone,cel,policy_privacy,agree_terms,email_recive_local,email_recive,status,newsletter_id,add_coupon,avatar,sex,notes,store_id,created_at; // string | Campos a serem retornados

try {
    $result = $apiInstance->promotionUsersIndex($promotion_id, $id, $external_id, $username, $email, $cpf, $_include, $_fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsuriosNaPromooApi->promotionUsersIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **id** | **int**| ID do usuário | [optional] |
| **external_id** | **string**| ID externo do usuário | [optional] |
| **username** | **string**| username do usuário | [optional] |
| **email** | **string**| email do usuário | [optional] |
| **cpf** | **string**| CPF do usuário | [optional] |
| **_include** | **string**| Dados relacionados a serem retornados | [optional] |
| **_fields** | **string**| Campos a serem retornados | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionUsersIndex200Response**](../Model/PromotionUsersIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionUsersUpdate()`

```php
promotionUsersUpdate($promotion_id, $promotion_users_create_request): \IdPluggerPromotion\Model\PromotionUsersUpdate201Response
```

Cadastra ou atualiza um usuário na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\UsuriosNaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$promotion_users_create_request = new \IdPluggerPromotion\Model\PromotionUsersCreateRequest(); // \IdPluggerPromotion\Model\PromotionUsersCreateRequest

try {
    $result = $apiInstance->promotionUsersUpdate($promotion_id, $promotion_users_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsuriosNaPromooApi->promotionUsersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **promotion_users_create_request** | [**\IdPluggerPromotion\Model\PromotionUsersCreateRequest**](../Model/PromotionUsersCreateRequest.md)|  | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionUsersUpdate201Response**](../Model/PromotionUsersUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promotionUsersWebhook()`

```php
promotionUsersWebhook($promotion_users_webhook_request): \IdPluggerPromotion\Model\PromotionUsersWebhook200Response
```
### URI(s):
- https://api.example.com/ URL do servidor do cliente
Webhook de resposta ao registro de usuário

Este endpoint é apenas um exemplo de como você receberá em seu webhook a notificação do registro de um usuário na promoção.  Em **Request body** clique em **Schema** para ver todos as variações de requisições que a API faz.  Alguns erros são apenas informativos de que alguma parte não essencial do cadastro não funcionou. Para identificar se o usuário foi cadastrado ou não, verifique se o parâmetro `content.id` está incluso na requisição e é um número maior que zero.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdPluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdPluggerPromotion\Api\UsuriosNaPromooApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_users_webhook_request = new \IdPluggerPromotion\Model\PromotionUsersWebhookRequest(); // \IdPluggerPromotion\Model\PromotionUsersWebhookRequest

$hostIndex = 0;
$variables = [
];

try {
    $result = $apiInstance->promotionUsersWebhook($promotion_users_webhook_request, $hostIndex, $variables);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsuriosNaPromooApi->promotionUsersWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_users_webhook_request** | [**\IdPluggerPromotion\Model\PromotionUsersWebhookRequest**](../Model/PromotionUsersWebhookRequest.md)|  | [optional] |
| hostIndex | null|int | Host index. Defaults to null. If null, then the library will use $this->hostIndex instead | [optional] |
| variables | array | Associative array of variables to pass to the host. Defaults to empty array. | [optional] |

### Return type

[**\IdPluggerPromotion\Model\PromotionUsersWebhook200Response**](../Model/PromotionUsersWebhook200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
