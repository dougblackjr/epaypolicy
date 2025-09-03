# Tns\EpayPolicy\TokensApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**tokensDelete()**](TokensApi.md#tokensDelete) | **DELETE** /api/v1/tokens/{id} | Removes a stored token. |
| [**tokensGet()**](TokensApi.md#tokensGet) | **GET** /api/v1/tokens/{id} | Retrieves the details of a token. |
| [**tokensPost()**](TokensApi.md#tokensPost) | **POST** /api/v1/tokens | Stores a token for either ACH or credit card payments. |


## `tokensDelete()`

```php
tokensDelete($id, $impersonation_account_key)
```

Removes a stored token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The public Id of the token to be deleted.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->tokensDelete($id, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->tokensDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The public Id of the token to be deleted. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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

## `tokensGet()`

```php
tokensGet($id, $impersonation_account_key): \Tns\EpayPolicy\Model\GetTokenResponseModel
```

Retrieves the details of a token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The public Id of the token.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $result = $apiInstance->tokensGet($id, $impersonation_account_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->tokensGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The public Id of the token. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

### Return type

[**\Tns\EpayPolicy\Model\GetTokenResponseModel**](../Model/GetTokenResponseModel.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `tokensPost()`

```php
tokensPost($post_token_request_model, $impersonation_account_key)
```

Stores a token for either ACH or credit card payments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_token_request_model = new \Tns\EpayPolicy\Model\PostTokenRequestModel(); // \Tns\EpayPolicy\Model\PostTokenRequestModel | The details of the token to be created. In the response, the Id of the created token is the last part of the URI in the location header attribute.
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->tokensPost($post_token_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->tokensPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_token_request_model** | [**\Tns\EpayPolicy\Model\PostTokenRequestModel**](../Model/PostTokenRequestModel.md)| The details of the token to be created. In the response, the Id of the created token is the last part of the URI in the location header attribute. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being processed. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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
