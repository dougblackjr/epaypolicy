# Tns\\EpayPolicy\ManagedInvoicesApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**managedInvoicesFinance()**](ManagedInvoicesApi.md#managedInvoicesFinance) | **POST** /api/v1/managedInvoices/{id}/finance | Creates Managed Invoice with Financing. |
| [**managedInvoicesGet()**](ManagedInvoicesApi.md#managedInvoicesGet) | **GET** /api/v1/managedInvoices/{id} | Retrieves the details of a managed invoice. |
| [**managedInvoicesPost()**](ManagedInvoicesApi.md#managedInvoicesPost) | **POST** /api/v1/managedInvoices | Creates Managed Invoice. |
| [**managedInvoicesSearch()**](ManagedInvoicesApi.md#managedInvoicesSearch) | **GET** /api/v1/managedInvoices | Retrieves a list of Managed invoices based on search parameters. |
| [**managedInvoicesVoid()**](ManagedInvoicesApi.md#managedInvoicesVoid) | **POST** /api/v1/managedInvoices/{id}/void | Processes a void of a managed invoice. |


## `managedInvoicesFinance()`

```php
managedInvoicesFinance($id, $post_create_managed_invoices_finance_request_model, $impersonation_account_key)
```

Creates Managed Invoice with Financing.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\ManagedInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The public id of the managed invoice to be edited.
$post_create_managed_invoices_finance_request_model = new \Tns\\EpayPolicy\Model\PostCreateManagedInvoicesFinanceRequestModel(); // \Tns\\EpayPolicy\Model\PostCreateManagedInvoicesFinanceRequestModel | The details of the Quote/Invoice to be created. In the response, the Id of the created Quote/Invoice is the last part of the URI in the location header attribute.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the quote/invoice is being created. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->managedInvoicesFinance($id, $post_create_managed_invoices_finance_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling ManagedInvoicesApi->managedInvoicesFinance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The public id of the managed invoice to be edited. | |
| **post_create_managed_invoices_finance_request_model** | [**\Tns\\EpayPolicy\Model\PostCreateManagedInvoicesFinanceRequestModel**](../Model/PostCreateManagedInvoicesFinanceRequestModel.md)| The details of the Quote/Invoice to be created. In the response, the Id of the created Quote/Invoice is the last part of the URI in the location header attribute. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the quote/invoice is being created. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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

## `managedInvoicesGet()`

```php
managedInvoicesGet($id, $impersonation_account_key): \Tns\\EpayPolicy\Model\GetManagedInvoiceResponseModel
```

Retrieves the details of a managed invoice.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\ManagedInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The Id or public Id of the managed invoice.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the managed is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->managedInvoicesGet($id, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedInvoicesApi->managedInvoicesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The Id or public Id of the managed invoice. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the managed is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\\EpayPolicy\Model\GetManagedInvoiceResponseModel**](../Model/GetManagedInvoiceResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `managedInvoicesPost()`

```php
managedInvoicesPost($post_create_managed_invoices_request_model, $impersonation_account_key)
```

Creates Managed Invoice.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\ManagedInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_create_managed_invoices_request_model = new \Tns\\EpayPolicy\Model\PostCreateManagedInvoicesRequestModel(); // \Tns\\EpayPolicy\Model\PostCreateManagedInvoicesRequestModel | The details of the Managed Invoice to be created. In the response, the Id of the created Managed Invoice is the last part of the URI in the location header attribute.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the managed invoice is being created. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->managedInvoicesPost($post_create_managed_invoices_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling ManagedInvoicesApi->managedInvoicesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_create_managed_invoices_request_model** | [**\Tns\\EpayPolicy\Model\PostCreateManagedInvoicesRequestModel**](../Model/PostCreateManagedInvoicesRequestModel.md)| The details of the Managed Invoice to be created. In the response, the Id of the created Managed Invoice is the last part of the URI in the location header attribute. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the managed invoice is being created. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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

## `managedInvoicesSearch()`

```php
managedInvoicesSearch($payer_name, $created_by, $due_date_from, $due_date_to, $managed_invoice_search_status_type, $page, $page_size, $impersonation_account_key): \Tns\\EpayPolicy\Model\GetManagedInvoicesResponseModel
```

Retrieves a list of Managed invoices based on search parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\ManagedInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payer_name = 'payer_name_example'; // string | When filtering by the payer's name, the name or partial name to match.
$created_by = 'created_by_example'; // string | When filtering by the creator's name, the name or partial name to match.
$due_date_from = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by due date, the earliest permitted date. Default is null.
$due_date_to = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by due date, the latest permitted date. Default is null.
$managed_invoice_search_status_type = 'managed_invoice_search_status_type_example'; // string | The type of managed invoice status search to perform. Default is open.
$page = 'page_example'; // string | The page of results to return. Default is 1.
$page_size = 'page_size_example'; // string | The size of each page. Default is 25, Maximum is 50.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the managed invoice is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->managedInvoicesSearch($payer_name, $created_by, $due_date_from, $due_date_to, $managed_invoice_search_status_type, $page, $page_size, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedInvoicesApi->managedInvoicesSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payer_name** | **string**| When filtering by the payer&#39;s name, the name or partial name to match. | [optional] |
| **created_by** | **string**| When filtering by the creator&#39;s name, the name or partial name to match. | [optional] |
| **due_date_from** | **\DateTime**| When filtering by due date, the earliest permitted date. Default is null. | [optional] |
| **due_date_to** | **\DateTime**| When filtering by due date, the latest permitted date. Default is null. | [optional] |
| **managed_invoice_search_status_type** | **string**| The type of managed invoice status search to perform. Default is open. | [optional] |
| **page** | **string**| The page of results to return. Default is 1. | [optional] |
| **page_size** | **string**| The size of each page. Default is 25, Maximum is 50. | [optional] |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the managed invoice is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\\EpayPolicy\Model\GetManagedInvoicesResponseModel**](../Model/GetManagedInvoicesResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `managedInvoicesVoid()`

```php
managedInvoicesVoid($id, $impersonation_account_key)
```

Processes a void of a managed invoice.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\ManagedInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The Id or public Id of the managed invoice to be voided.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the managed invoice is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->managedInvoicesVoid($id, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling ManagedInvoicesApi->managedInvoicesVoid: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The Id or public Id of the managed invoice to be voided. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the managed invoice is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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
