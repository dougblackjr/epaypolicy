# Tns\\EpayPolicy\TransactionsApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**transactionsAuthorize()**](TransactionsApi.md#transactionsAuthorize) | **POST** /api/v1/transactions/authorize | Creates an authorization on a credit card. |
| [**transactionsGet()**](TransactionsApi.md#transactionsGet) | **GET** /api/v1/transactions/{id} | Retrieves the details of a transaction. |
| [**transactionsPost()**](TransactionsApi.md#transactionsPost) | **POST** /api/v1/transactions | Processes a sale transaction for either ACH or credit card. |
| [**transactionsRefund()**](TransactionsApi.md#transactionsRefund) | **POST** /api/v1/transactions/{id}/refund | Processes a refund of a transaction. |
| [**transactionsSearch()**](TransactionsApi.md#transactionsSearch) | **GET** /api/v1/transactions | Retrieves a list of Transactions based on search parameters. |
| [**transactionsVoid()**](TransactionsApi.md#transactionsVoid) | **POST** /api/v1/transactions/{id}/void | Processes a void of a transaction. |


## `transactionsAuthorize()`

```php
transactionsAuthorize($post_authorize_transaction_request_model, $impersonation_account_key)
```

Creates an authorization on a credit card.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_authorize_transaction_request_model = new \Tns\\EpayPolicy\Model\PostAuthorizeTransactionRequestModel(); // \Tns\\EpayPolicy\Model\PostAuthorizeTransactionRequestModel | The details of the transaction to be authorized.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->transactionsAuthorize($post_authorize_transaction_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->transactionsAuthorize: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_authorize_transaction_request_model** | [**\Tns\\EpayPolicy\Model\PostAuthorizeTransactionRequestModel**](../Model/PostAuthorizeTransactionRequestModel.md)| The details of the transaction to be authorized. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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

## `transactionsGet()`

```php
transactionsGet($id, $impersonation_account_key): \Tns\\EpayPolicy\Model\GetTransactionResponseModel
```

Retrieves the details of a transaction.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The Id of the transaction.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->transactionsGet($id, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->transactionsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The Id of the transaction. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\\EpayPolicy\Model\GetTransactionResponseModel**](../Model/GetTransactionResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionsPost()`

```php
transactionsPost($post_transaction_request_model, $impersonation_account_key)
```

Processes a sale transaction for either ACH or credit card.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_transaction_request_model = new \Tns\\EpayPolicy\Model\PostTransactionRequestModelV1(); // \Tns\\EpayPolicy\Model\PostTransactionRequestModelV1 | The details of the transaction to be processed. In the response, the Id of the created transaction is the last part of the URI in the location header attribute.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->transactionsPost($post_transaction_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->transactionsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_transaction_request_model** | [**\Tns\\EpayPolicy\Model\PostTransactionRequestModelV1**](../Model/PostTransactionRequestModelV1.md)| The details of the transaction to be processed. In the response, the Id of the created transaction is the last part of the URI in the location header attribute. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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

## `transactionsRefund()`

```php
transactionsRefund($id, $post_refund_transaction_request_model, $impersonation_account_key)
```

Processes a refund of a transaction.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The Id of the transaction.
$post_refund_transaction_request_model = new \Tns\\EpayPolicy\Model\PostRefundTransactionRequestModel(); // \Tns\\EpayPolicy\Model\PostRefundTransactionRequestModel | The details of how to process the refund.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->transactionsRefund($id, $post_refund_transaction_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->transactionsRefund: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The Id of the transaction. | |
| **post_refund_transaction_request_model** | [**\Tns\\EpayPolicy\Model\PostRefundTransactionRequestModel**](../Model/PostRefundTransactionRequestModel.md)| The details of how to process the refund. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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

## `transactionsSearch()`

```php
transactionsSearch($begin_date, $end_date, $begin_create_date, $end_create_date, $transaction_search_type_id, $min_amount, $max_amount, $account_number, $payer_name, $batch_id, $page, $page_size, $impersonation_account_key): \Tns\\EpayPolicy\Model\GetTransactionsResponseModel
```

Retrieves a list of Transactions based on search parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$begin_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by date, the earliest permitted date. Default is 30 days ago. This parameter is ignored if beginCreateDate or endCreateDate is provided.
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by date, the latest permitted date. Default is now. This parameter is ignored if beginCreateDate or endCreateDate is provided.
$begin_create_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by create date, the earliest permitted date. Default is null, unless endCreateDate provided then default is 30 days ago.
$end_create_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When filtering by create date, the latest permitted date. Default is null.
$transaction_search_type_id = 'transaction_search_type_id_example'; // string | The type of transaction search to perform. Default is Processed.
$min_amount = 3.4; // float | When filtering by amount, the minimum permitted amount.
$max_amount = 3.4; // float | When filtering by amount, the maximum permitted amount.
$account_number = 'account_number_example'; // string | When filtering by payment method details, the last four digits of the payment method's account number.
$payer_name = 'payer_name_example'; // string | When filtering by the payer's name, the name or partial name to match.
$batch_id = 56; // int | When filtering by batch, the id of the batch.
$page = 56; // int | The page of results to return. Default is 1.
$page_size = 'page_size_example'; // string | The size of each page. Default is 25, Maximum is 50.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->transactionsSearch($begin_date, $end_date, $begin_create_date, $end_create_date, $transaction_search_type_id, $min_amount, $max_amount, $account_number, $payer_name, $batch_id, $page, $page_size, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->transactionsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **begin_date** | **\DateTime**| When filtering by date, the earliest permitted date. Default is 30 days ago. This parameter is ignored if beginCreateDate or endCreateDate is provided. | [optional] |
| **end_date** | **\DateTime**| When filtering by date, the latest permitted date. Default is now. This parameter is ignored if beginCreateDate or endCreateDate is provided. | [optional] |
| **begin_create_date** | **\DateTime**| When filtering by create date, the earliest permitted date. Default is null, unless endCreateDate provided then default is 30 days ago. | [optional] |
| **end_create_date** | **\DateTime**| When filtering by create date, the latest permitted date. Default is null. | [optional] |
| **transaction_search_type_id** | **string**| The type of transaction search to perform. Default is Processed. | [optional] |
| **min_amount** | **float**| When filtering by amount, the minimum permitted amount. | [optional] |
| **max_amount** | **float**| When filtering by amount, the maximum permitted amount. | [optional] |
| **account_number** | **string**| When filtering by payment method details, the last four digits of the payment method&#39;s account number. | [optional] |
| **payer_name** | **string**| When filtering by the payer&#39;s name, the name or partial name to match. | [optional] |
| **batch_id** | **int**| When filtering by batch, the id of the batch. | [optional] |
| **page** | **int**| The page of results to return. Default is 1. | [optional] |
| **page_size** | **string**| The size of each page. Default is 25, Maximum is 50. | [optional] |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\\EpayPolicy\Model\GetTransactionsResponseModel**](../Model/GetTransactionsResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `transactionsVoid()`

```php
transactionsVoid($id, $post_void_transaction_request_model, $send_receipt, $impersonation_account_key)
```

Processes a void of a transaction.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The Id of the transaction.
$post_void_transaction_request_model = new \Tns\\EpayPolicy\Model\PostVoidTransactionRequestModel(); // \Tns\\EpayPolicy\Model\PostVoidTransactionRequestModel | The details of how to process the void.
$send_receipt = True; // bool | [Deprecated. Please use the postVoidTransactionRequestModel parameter.] Set to true if a receipt should be sent to all parties upon a successful void.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->transactionsVoid($id, $post_void_transaction_request_model, $send_receipt, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->transactionsVoid: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The Id of the transaction. | |
| **post_void_transaction_request_model** | [**\Tns\\EpayPolicy\Model\PostVoidTransactionRequestModel**](../Model/PostVoidTransactionRequestModel.md)| The details of how to process the void. | |
| **send_receipt** | **bool**| [Deprecated. Please use the postVoidTransactionRequestModel parameter.] Set to true if a receipt should be sent to all parties upon a successful void. | [optional] |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the transaction is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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
