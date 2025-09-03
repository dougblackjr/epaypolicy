# Tns\EpayPolicy\AutoPayApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**autoPayCancel()**](AutoPayApi.md#autoPayCancel) | **POST** /api/v1/autoPay/{id}/cancel | Cancels an active Auto Pay. |
| [**autoPayGet()**](AutoPayApi.md#autoPayGet) | **GET** /api/v1/autoPay/{id} | Retrieves the details of an AutoPay. |
| [**autoPayPost()**](AutoPayApi.md#autoPayPost) | **POST** /api/v1/autoPay | Creates an Auto Pay. |
| [**autoPaySearch()**](AutoPayApi.md#autoPaySearch) | **GET** /api/v1/autoPays | Retrieves a list of auto pays based on search parameters. |


## `autoPayCancel()`

```php
autoPayCancel($id, $impersonation_account_key)
```

Cancels an active Auto Pay.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\AutoPayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The Id of the AutoPay.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction(s) will be processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->autoPayCancel($id, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling AutoPayApi->autoPayCancel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The Id of the AutoPay. | |
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

## `autoPayGet()`

```php
autoPayGet($id, $impersonation_account_key): \Tns\EpayPolicy\Model\GetAutoPayResponseModel
```

Retrieves the details of an AutoPay.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\AutoPayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The Id of the AutoPay.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->autoPayGet($id, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoPayApi->autoPayGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The Id of the AutoPay. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\EpayPolicy\Model\GetAutoPayResponseModel**](../Model/GetAutoPayResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `autoPayPost()`

```php
autoPayPost($post_auto_pay_request_model, $impersonation_account_key)
```

Creates an Auto Pay.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\AutoPayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_auto_pay_request_model = new \Tns\EpayPolicy\Model\PostAutoPayRequestModel(); // \Tns\EpayPolicy\Model\PostAutoPayRequestModel | Contains the parameters for the auto pay. In the response, the Id of the created auto pay is the last part of the URI in the location header attribute.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction(s) will be processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->autoPayPost($post_auto_pay_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling AutoPayApi->autoPayPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_auto_pay_request_model** | [**\Tns\EpayPolicy\Model\PostAutoPayRequestModel**](../Model/PostAutoPayRequestModel.md)| Contains the parameters for the auto pay. In the response, the Id of the created auto pay is the last part of the URI in the location header attribute. | |
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

## `autoPaySearch()`

```php
autoPaySearch($create_date_start, $create_date_end, $cancel_date_start, $cancel_date_end, $page, $page_size, $impersonation_account_key): \Tns\EpayPolicy\Model\GetAutoPaysResponseModel
```

Retrieves a list of auto pays based on search parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\AutoPayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_date_start = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by create date, the earliest permitted date. Default is 30 days ago.
$create_date_end = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by create date, the latest permitted date. Default is now.
$cancel_date_start = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by cancel date, the earliest permitted date. Default is 30 days ago.
$cancel_date_end = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by cancel date, the latest permitted date. Default is now.
$page = 56; // int | The page of results to return. Default is 1.
$page_size = 'page_size_example'; // string | The size of each page. Default is 25, Maximum is 50.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->autoPaySearch($create_date_start, $create_date_end, $cancel_date_start, $cancel_date_end, $page, $page_size, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoPayApi->autoPaySearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_date_start** | **\DateTime**| When filtering by create date, the earliest permitted date. Default is 30 days ago. | [optional] |
| **create_date_end** | **\DateTime**| When filtering by create date, the latest permitted date. Default is now. | [optional] |
| **cancel_date_start** | **\DateTime**| When filtering by cancel date, the earliest permitted date. Default is 30 days ago. | [optional] |
| **cancel_date_end** | **\DateTime**| When filtering by cancel date, the latest permitted date. Default is now. | [optional] |
| **page** | **int**| The page of results to return. Default is 1. | [optional] |
| **page_size** | **string**| The size of each page. Default is 25, Maximum is 50. | [optional] |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\EpayPolicy\Model\GetAutoPaysResponseModel**](../Model/GetAutoPaysResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
