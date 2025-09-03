# Tns\EpayPolicy\FinanceApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**financeConvertQuote()**](FinanceApi.md#financeConvertQuote) | **POST** /api/v1/Finance/ConvertQuote | ConvertQuote is to convert the given Quote and Creates an AutoPay subscription |


## `financeConvertQuote()`

```php
financeConvertQuote($post_convert_quote_request_model, $impersonation_account_key): object
```

ConvertQuote is to convert the given Quote and Creates an AutoPay subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\FinanceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_convert_quote_request_model = new \Tns\EpayPolicy\Model\PostConvertQuoteRequestModel(); // \Tns\EpayPolicy\Model\PostConvertQuoteRequestModel | Request model which consists of QuoteNumber, TransactionId and AttributeValues
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->financeConvertQuote($post_convert_quote_request_model, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FinanceApi->financeConvertQuote: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_convert_quote_request_model** | [**\Tns\EpayPolicy\Model\PostConvertQuoteRequestModel**](../Model/PostConvertQuoteRequestModel.md)| Request model which consists of QuoteNumber, TransactionId and AttributeValues | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

**object**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
