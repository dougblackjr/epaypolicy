# # UpdateInvoicesRequestModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The unique identifier for the transaction. | [optional]
**payer** | **string** | The name of the payer initiating the transaction. | [optional]
**email_address** | **string** | The email address of the payer. | [optional]
**paid_invoices** | [**\Tns\\EpayPolicy\Model\PaidInvoiceModel[]**](PaidInvoiceModel.md) | The collection of paid invoices with amounts and comments. | [optional]
**attribute_values** | **array<string,string>** | The list of attribute values that uniquely identify this payer in the underlying accounting system. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
