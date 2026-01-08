# IdpluggerPromotion\UsersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**usersCreate()**](UsersApi.md#usersCreate) | **POST** /v3/promotion/{promotion_id}/users | Cadastra um usuário na promoção |
| [**usersDelete()**](UsersApi.md#usersDelete) | **DELETE** /v3/promotion/{promotion_id}/users/{user_id} | Exclui um usuário da promoção |
| [**usersIndex()**](UsersApi.md#usersIndex) | **GET** /v3/promotion/{promotion_id}/users | Busca por um usuário cadastrado na promoção |
| [**usersUpdate()**](UsersApi.md#usersUpdate) | **PATCH** /v3/promotion/{promotion_id}/users | Cadastra ou atualiza um usuário na promoção |
| [**usersWebhook()**](UsersApi.md#usersWebhook) | **POST** /webhook-do-usuario | Webhook de resposta ao registro de usuário |


## `usersCreate()`

```php
usersCreate($promotion_id, $users_create_request): \IdpluggerPromotion\Model\UsersCreate201Response
```

Cadastra um usuário na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$users_create_request = new \IdpluggerPromotion\Model\UsersCreateRequest(); // \IdpluggerPromotion\Model\UsersCreateRequest

try {
    $result = $apiInstance->usersCreate($promotion_id, $users_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **users_create_request** | [**\IdpluggerPromotion\Model\UsersCreateRequest**](../Model/UsersCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\UsersCreate201Response**](../Model/UsersCreate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersDelete()`

```php
usersDelete($promotion_id, $user_id): \IdpluggerPromotion\Model\UsersDelete200Response
```

Exclui um usuário da promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$user_id = 'user_id_example'; // string | ID do usuário

try {
    $result = $apiInstance->usersDelete($promotion_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **user_id** | **string**| ID do usuário | |

### Return type

[**\IdpluggerPromotion\Model\UsersDelete200Response**](../Model/UsersDelete200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersIndex()`

```php
usersIndex($promotion_id, $id, $external_id, $username, $email, $cpf, $_include, $_fields, $page, $_per_page): \IdpluggerPromotion\Model\UsersIndex200Response
```

Busca por um usuário cadastrado na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\UsersApi(
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
$page = 1; // int | Informa o número da página da pesquisa
$_per_page = 1; // int | Informa o número de itens por página na pesquisa

try {
    $result = $apiInstance->usersIndex($promotion_id, $id, $external_id, $username, $email, $cpf, $_include, $_fields, $page, $_per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersIndex: ', $e->getMessage(), PHP_EOL;
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
| **page** | **int**| Informa o número da página da pesquisa | [optional] |
| **_per_page** | **int**| Informa o número de itens por página na pesquisa | [optional] |

### Return type

[**\IdpluggerPromotion\Model\UsersIndex200Response**](../Model/UsersIndex200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersUpdate()`

```php
usersUpdate($promotion_id, $users_create_request): \IdpluggerPromotion\Model\UsersUpdate201Response
```

Cadastra ou atualiza um usuário na promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$users_create_request = new \IdpluggerPromotion\Model\UsersCreateRequest(); // \IdpluggerPromotion\Model\UsersCreateRequest

try {
    $result = $apiInstance->usersUpdate($promotion_id, $users_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **users_create_request** | [**\IdpluggerPromotion\Model\UsersCreateRequest**](../Model/UsersCreateRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\UsersUpdate201Response**](../Model/UsersUpdate201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `usersWebhook()`

```php
usersWebhook($users_webhook_request): \IdpluggerPromotion\Model\UsersWebhook200Response
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
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\UsersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$users_webhook_request = new \IdpluggerPromotion\Model\UsersWebhookRequest(); // \IdpluggerPromotion\Model\UsersWebhookRequest

$hostIndex = 0;
$variables = [
];

try {
    $result = $apiInstance->usersWebhook($users_webhook_request, $hostIndex, $variables);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **users_webhook_request** | [**\IdpluggerPromotion\Model\UsersWebhookRequest**](../Model/UsersWebhookRequest.md)|  | [optional] |
| hostIndex | null|int | Host index. Defaults to null. If null, then the library will use $this->hostIndex instead | [optional] |
| variables | array | Associative array of variables to pass to the host. Defaults to empty array. | [optional] |

### Return type

[**\IdpluggerPromotion\Model\UsersWebhook200Response**](../Model/UsersWebhook200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
