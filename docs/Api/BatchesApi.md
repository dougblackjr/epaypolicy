# Tns\EpayPolicy\BatchesApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchesGet()**](BatchesApi.md#batchesGet) | **GET** /api/v1/batches | Gets a collection of Batches. |


## `batchesGet()`

```php
batchesGet($page, $impersonation_account_key): \Tns\EpayPolicy\Model\GetBatchesResponseModel
```

Gets a collection of Batches.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\BatchesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int | The page of results to return. Default is 1.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the batches were processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->batchesGet($page, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->batchesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The page of results to return. Default is 1. | [optional] |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the batches were processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\EpayPolicy\Model\GetBatchesResponseModel**](../Model/GetBatchesResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
