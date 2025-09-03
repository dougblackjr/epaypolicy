# # PostTokenRequestModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payer** | **string** | Name of the payer that is storing the token. |
**email_address** | **string** | The email address of the payer. |
**credit_card_information** | [**\Tns\EpayPolicy\Model\CreditCardInformationModel**](CreditCardInformationModel.md) |  | [optional]
**bank_account_information** | [**\Tns\EpayPolicy\Model\BankAccountInformationModel**](BankAccountInformationModel.md) |  | [optional]
**attribute_values** | **array<string,string>** | Dictionary of custom attribute values. The key in the dictionary is the identifier of the custom attribute. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
