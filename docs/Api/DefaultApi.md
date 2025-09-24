# IdpluggerPromotion\DefaultApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v3PromotionPromotionIdCouponsGet()**](DefaultApi.md#v3PromotionPromotionIdCouponsGet) | **GET** /v3/promotion/{promotion_id}/coupons | Buscar cupons de uma promoção |


## `v3PromotionPromotionIdCouponsGet()`

```php
v3PromotionPromotionIdCouponsGet($promotion_id, $_fields, $_include, $id, $user_id, $external_user_id, $purchase_date, $insert_at, $tax_coupon): \IdpluggerPromotion\Model\V3PromotionPromotionIdCouponsGet200Response
```

Buscar cupons de uma promoção

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = IdpluggerPromotion\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new IdpluggerPromotion\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$promotion_id = 'promotion_id_example'; // string
$_fields = id,taxcoupon; // string
$_include = custom_data,lucky_numbers,serial_numbers,products; // string
$id = 1; // int
$user_id = 1; // int
$external_user_id = user_1; // string
$purchase_date = 2025-06-13 00:00:00 AND 2025-06-13 23:59:59; // string
$insert_at = 2025-06-23 00:00:00 AND 2025-06-23 23:59:59; // string
$tax_coupon = 160630; // int

try {
    $result = $apiInstance->v3PromotionPromotionIdCouponsGet($promotion_id, $_fields, $_include, $id, $user_id, $external_user_id, $purchase_date, $insert_at, $tax_coupon);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->v3PromotionPromotionIdCouponsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **promotion_id** | **string**|  | |
| **_fields** | **string**|  | [optional] |
| **_include** | **string**|  | [optional] |
| **id** | **int**|  | [optional] |
| **user_id** | **int**|  | [optional] |
| **external_user_id** | **string**|  | [optional] |
| **purchase_date** | **string**|  | [optional] |
| **insert_at** | **string**|  | [optional] |
| **tax_coupon** | **int**|  | [optional] |

### Return type

[**\IdpluggerPromotion\Model\V3PromotionPromotionIdCouponsGet200Response**](../Model/V3PromotionPromotionIdCouponsGet200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
