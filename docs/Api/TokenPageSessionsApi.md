# Tns\EpayPolicy\TokenPageSessionsApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**tokenPageSessionsPost()**](TokenPageSessionsApi.md#tokenPageSessionsPost) | **POST** /api/v1/tokenPageSessions | Creates a temporary \&quot;session\&quot; with parameters so that the user can be forwarded to the token page with this context. |


## `tokenPageSessionsPost()`

```php
tokenPageSessionsPost($post_token_page_session_request_model, $impersonation_account_key)
```

Creates a temporary \"session\" with parameters so that the user can be forwarded to the token page with this context.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\EpayPolicy\Api\TokenPageSessionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_token_page_session_request_model = new \Tns\EpayPolicy\Model\PostTokenPageSessionRequestModel(); // \Tns\EpayPolicy\Model\PostTokenPageSessionRequestModel | Contains the parameters for the \"session\".
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being created. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->tokenPageSessionsPost($post_token_page_session_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling TokenPageSessionsApi->tokenPageSessionsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_token_page_session_request_model** | [**\Tns\EpayPolicy\Model\PostTokenPageSessionRequestModel**](../Model/PostTokenPageSessionRequestModel.md)| Contains the parameters for the \&quot;session\&quot;. | |
| **impersonation_account_key** | **string**| The key that allows impersonation of another account for which the token is being created. Only specify a value if the account being impersonated is different from the account that is submitting this request. | [optional] |

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
