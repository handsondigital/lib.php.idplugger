# IdpluggerPromotion\FilesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**filesShow()**](FilesApi.md#filesShow) | **GET** /v3/{promotion_id}/files/{filename} | Faz o download de um arquivo |


## `filesShow()`

```php
filesShow($promotion_id, $filename)
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
    $apiInstance->filesShow($promotion_id, $filename);
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

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
