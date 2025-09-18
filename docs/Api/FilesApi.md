# IdpluggerPromotion\FilesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**filesShow()**](FilesApi.md#filesShow) | **GET** /v3/promotion/{promotion_id}/files/{filename} | Faz o download de um arquivo |


## `filesShow()`

```php
filesShow($promotion_id, $filename): \IdpluggerPromotion\Model\FilesShow200Response
```

Faz o download de um arquivo

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new IdpluggerPromotion\Api\FilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$promotion_id = 'promotion_id_example'; // string | ID da promoção
$filename = 'filename_example'; // string | Nome do arquivo

try {
    $result = $apiInstance->filesShow($promotion_id, $filename);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilesApi->filesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**| ID da promoção | |
| **filename** | **string**| Nome do arquivo | |

### Return type

[**\IdpluggerPromotion\Model\FilesShow200Response**](../Model/FilesShow200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
