# # GetTokenResponseModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The public Id of the token. | [optional]
**payer** | **string** | The name of the payer. | [optional]
**email_address** | **string** | The email address of the payer. | [optional]
**attribute_values** | [**\Tns\EpayPolicy\Model\AttributeValueModel[]**](AttributeValueModel.md) | A collection of key/value pairs for any custom attribute values for this token. | [optional]
**transaction_type** | **string** | The type of transaction. | [optional]
**masked_account_number** | **string** | The masked account number for display to the user. | [optional]
**country** | **string** | The country of the token | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
