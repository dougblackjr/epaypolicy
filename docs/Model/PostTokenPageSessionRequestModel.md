# # PostTokenPageSessionRequestModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attribute_values** | **array<string,string>** | Key/value collection of all custom attributes that will eventually be stored with the token. | [optional]
**success_url** | **string** | The Url to which the user will be redirected upon a token being successfully created. | [optional]
**accepted_payment_methods** | **string[]** | A white-list of accepted payment methods that should be shown on the token page. If none are provided, all payment methods will be enabled. &#x3D; [&#39;CreditCard&#39;, &#39;Ach&#39;] | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
