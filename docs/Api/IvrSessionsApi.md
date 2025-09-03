# Tns\\EpayPolicy\IvrSessionsApi

All URIs are relative to https://api-sandbox.epaypolicy.com:443, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**ivrSessionsPost()**](IvrSessionsApi.md#ivrSessionsPost) | **POST** /api/v1/ivrSessions | Creates a temporary \&quot;session\&quot; with parameters so that the caller can be forwarded to the IVR service with this context. |


## `ivrSessionsPost()`

```php
ivrSessionsPost($post_ivr_session_request_model, $impersonation_account_key)
```

Creates a temporary \"session\" with parameters so that the caller can be forwarded to the IVR service with this context.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basic
$config = Tns\\EpayPolicy\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Tns\\EpayPolicy\Api\IvrSessionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_ivr_session_request_model = new \Tns\\EpayPolicy\Model\PostIvrSessionRequestModel(); // \Tns\\EpayPolicy\Model\PostIvrSessionRequestModel | Contains the parameters for the \"session\".
$impersonation_account_key = 'impersonation_account_key_example'; // string | The key that allows impersonation of another account for which the token is being created. Only specify a value if the account being impersonated is different from the account that is submitting this request.

try {
    $apiInstance->ivrSessionsPost($post_ivr_session_request_model, $impersonation_account_key);
} catch (Exception $e) {
    echo 'Exception when calling IvrSessionsApi->ivrSessionsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_ivr_session_request_model** | [**\Tns\\EpayPolicy\Model\PostIvrSessionRequestModel**](../Model/PostIvrSessionRequestModel.md)| Contains the parameters for the \&quot;session\&quot;. | |
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
