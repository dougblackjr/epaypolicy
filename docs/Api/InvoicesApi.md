# Tns\\EpayPolicy\InvoicesApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**invoicesEmail()**](InvoicesApi.md#invoicesEmail) | **POST** /api/v1/Invoices/Email | Sends an email for a collection of invoices in the management system. |
| [**invoicesGet()**](InvoicesApi.md#invoicesGet) | **GET** /api/v1/Invoices | Gets a collection of invoices given lookup attributes. Add these attributes as individual parameters. |
| [**invoicesPayments()**](InvoicesApi.md#invoicesPayments) | **POST** /api/v1/Invoices/Payments | Updates a collection of invoices in the management system. |
| [**invoicesUpdate()**](InvoicesApi.md#invoicesUpdate) | **POST** /api/v1/Invoices | Updates a collection of invoices in the management system. |


## `invoicesEmail()`

```php
invoicesEmail($post_send_invoice_email_request_model, $impersonation_account_key)
```

Sends an email for a collection of invoices in the management system.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_send_invoice_email_request_model = new \Tns\\EpayPolicy\Model\PostSendInvoiceEmailRequestModel(); // \Tns\\EpayPolicy\Model\PostSendInvoiceEmailRequestModel | The Invoice lookup attributes.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The impersonation account key.

try {
    $apiInstance->invoicesEmail($post_send_invoice_email_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesEmail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_send_invoice_email_request_model** | [**\Tns\\EpayPolicy\Model\PostSendInvoiceEmailRequestModel**](../Model/PostSendInvoiceEmailRequestModel.md)| The Invoice lookup attributes. | |
| **impersonation_account_key** | **string**| The impersonation account key. | [optional] |

### Return type

void (empty response body)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesGet()`

```php
invoicesGet($impersonation_account_key)
```

Gets a collection of invoices given lookup attributes. Add these attributes as individual parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$impersonation_account_key = 'impersonation_account_key_example'; // string

try {
    $apiInstance->invoicesGet($impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **impersonation_account_key** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesPayments()`

```php
invoicesPayments($update_invoices_request_model, $impersonation_account_key)
```

Updates a collection of invoices in the management system.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$update_invoices_request_model = new \Tns\\EpayPolicy\Model\UpdateInvoicesRequestModel(); // \Tns\\EpayPolicy\Model\UpdateInvoicesRequestModel | The paid invoices and lookup attributes.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The impersonation account key.

try {
    $apiInstance->invoicesPayments($update_invoices_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesPayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_invoices_request_model** | [**\Tns\\EpayPolicy\Model\UpdateInvoicesRequestModel**](../Model/UpdateInvoicesRequestModel.md)| The paid invoices and lookup attributes. | |
| **impersonation_account_key** | **string**| The impersonation account key. | [optional] |

### Return type

void (empty response body)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `invoicesUpdate()`

```php
invoicesUpdate($api_version, $update_invoices_request_model, $impersonation_account_key)
```

Updates a collection of invoices in the management system.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_version = 'api_version_example'; // string
$update_invoices_request_model = new \Tns\\EpayPolicy\Model\UpdateInvoicesRequestModel(); // \Tns\\EpayPolicy\Model\UpdateInvoicesRequestModel | The paid invoices and lookup attributes.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The impersonation account key.

try {
    $apiInstance->invoicesUpdate($api_version, $update_invoices_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->invoicesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_version** | **string**|  | |
| **update_invoices_request_model** | [**\Tns\\EpayPolicy\Model\UpdateInvoicesRequestModel**](../Model/UpdateInvoicesRequestModel.md)| The paid invoices and lookup attributes. | |
| **impersonation_account_key** | **string**| The impersonation account key. | [optional] |

### Return type

void (empty response body)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
