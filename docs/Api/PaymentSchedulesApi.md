# Tns\\EpayPolicy\PaymentSchedulesApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**paymentSchedulesCancel()**](PaymentSchedulesApi.md#paymentSchedulesCancel) | **POST** /api/v1/paymentSchedules/{id}/cancel | Cancels an active payment schedule. |
| [**paymentSchedulesGet()**](PaymentSchedulesApi.md#paymentSchedulesGet) | **GET** /api/v1/paymentSchedules/{id} | Retrieves the details of a payment schedule. |
| [**paymentSchedulesPost()**](PaymentSchedulesApi.md#paymentSchedulesPost) | **POST** /api/v1/paymentSchedules | Creates a payment schedule for a delayed payment or recurring payments. |


## `paymentSchedulesCancel()`

```php
paymentSchedulesCancel($id, $impersonation_account_key)
```

Cancels an active payment schedule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\PaymentSchedulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The public Id of the payment schedule.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction(s) will be processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->paymentSchedulesCancel($id, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling PaymentSchedulesApi->paymentSchedulesCancel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The public Id of the payment schedule. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction(s) will be processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

void (empty response body)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentSchedulesGet()`

```php
paymentSchedulesGet($id, $impersonation_account_key): \Tns\\EpayPolicy\Model\GetPaymentScheduleResponseModel
```

Retrieves the details of a payment schedule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\PaymentSchedulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The public Id of the payment schedule.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->paymentSchedulesGet($id, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentSchedulesApi->paymentSchedulesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The public Id of the payment schedule. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\\EpayPolicy\Model\GetPaymentScheduleResponseModel**](../Model/GetPaymentScheduleResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `paymentSchedulesPost()`

```php
paymentSchedulesPost($post_payment_schedule_request_model, $impersonation_account_key)
```

Creates a payment schedule for a delayed payment or recurring payments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\PaymentSchedulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_payment_schedule_request_model = new \Tns\\EpayPolicy\Model\PostPaymentScheduleRequestModel(); // \Tns\\EpayPolicy\Model\PostPaymentScheduleRequestModel | Contains the parameters for the payment schedule. In the response, the Id of the created payment schedule is the last part of the URI in the location header attribute.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction(s) will be processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->paymentSchedulesPost($post_payment_schedule_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling PaymentSchedulesApi->paymentSchedulesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_payment_schedule_request_model** | [**\Tns\\EpayPolicy\Model\PostPaymentScheduleRequestModel**](../Model/PostPaymentScheduleRequestModel.md)| Contains the parameters for the payment schedule. In the response, the Id of the created payment schedule is the last part of the URI in the location header attribute. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction(s) will be processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

void (empty response body)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
