# # PostTransactionRequestModelV1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **float** | Total amount to charge not including any payer fees. |
**payer** | **string** | Name of the payer that is shown on the receipt. |
**payer_fee** | **float** | Used if the calling application has pre-calculated a payer fee. In that case, the fee will not be re-calculated. | [optional]
**attribute_values** | **array<string,string>** | Dictionary of custom attribute values. The key in the dictionary is the identifier of the custom attribute. | [optional]
**comments** | **string** | Comments that are shown on the receipt. | [optional]
**email_address** | **string** | The recipient of the emailed receipt. |
**token_id** | **string** | Used to reference a previously stored payment token. | [optional]
**credit_card_information** | [**\Tns\EpayPolicy\Model\CreditCardInformationModel**](CreditCardInformationModel.md) |  | [optional]
**bank_account_information** | [**\Tns\EpayPolicy\Model\BankAccountInformationModel**](BankAccountInformationModel.md) |  | [optional]
**authorization_id** | **string** | Used when executing a capture on authorizations that were obtained via this service. | [optional]
**send_receipt** | **bool** | Set to true if the payer and account holder(s) should receive an e-receipt. | [optional]
**initiating_party_fee** | **float** | The fee being charged by the initiating party of this transaction. This does not include the standard transaction fees. | [optional]
**ip_address** | **string** | The IP Address of the payer. | [optional]
**currency** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
