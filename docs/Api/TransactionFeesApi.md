# Tns\EpayPolicy\TransactionFeesApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**transactionFeesGet()**](TransactionFeesApi.md#transactionFeesGet) | **GET** /api/v1/transactionFees | Calculates and returns transaction fees for a given net amount due based on the account. |


## `transactionFeesGet()`

```php
transactionFeesGet($amount, $impersonation_account_key): \Tns\EpayPolicy\Model\GetTransactionFeesResponseModel
```

Calculates and returns transaction fees for a given net amount due based on the account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\TransactionFeesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$amount = 3.4; // float | Net amount due from which to calculate the transaction fees.
$impersonation_account_key = 'impersonation_account_key_example'; // string

try {
    $result = $apiInstance->transactionFeesGet($amount, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionFeesApi->transactionFeesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **amount** | **float**| Net amount due from which to calculate the transaction fees. | |
| **impersonation_account_key** | **string**|  | [optional] |

### Return type

[**\Tns\EpayPolicy\Model\GetTransactionFeesResponseModel**](../Model/GetTransactionFeesResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
