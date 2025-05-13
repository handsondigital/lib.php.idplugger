# IdpluggerPromotion\SettingsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**configWebhook()**](SettingsApi.md#configWebhook) | **POST** /v3/promotion/{promotion_id}/webhook | Configura o webhook da promoção |


## `configWebhook()`

```php
configWebhook($promotion_id, $config_webhook_request): \IdpluggerPromotion\Model\ConfigWebhook200Response
```

Configura o webhook da promoção

Este endpoint é responsável por configurar o webhook da promoção. Ao cadastrar um usuário ou um cupom na promoção, a API irá armazenar estas informações para processar em segundo plano. Ao fim do processamento (ou em caso de falha) do cadastro a API irá fazer uma requisição do tipo POST para o webhook configurado.  O `secret` cadastrado será enviado através do header `authorization`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$config_webhook_request = new \IdpluggerPromotion\Model\ConfigWebhookRequest(); // \IdpluggerPromotion\Model\ConfigWebhookRequest

try {
    $result = $apiInstance->configWebhook($promotion_id, $config_webhook_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->configWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **config_webhook_request** | [**\IdpluggerPromotion\Model\ConfigWebhookRequest**](../Model/ConfigWebhookRequest.md)|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\ConfigWebhook200Response**](../Model/ConfigWebhook200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
