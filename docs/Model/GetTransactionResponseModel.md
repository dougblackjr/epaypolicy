# # GetTransactionResponseModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The Id of the transaction. | [optional]
**public_id** | **string** | The PublicId of the transaction | [optional]
**payer** | **string** | The name of the payer. | [optional]
**email_address** | **string** | The email address of the payer. | [optional]
**transaction_type** | **string** | The type of the transaction. | [optional]
**amount** | **float** | The total amount of the transaction that was charged to the payer including all fees. | [optional]
**fee** | **float** | The transaction fee charged. | [optional]
**payer_fee** | **float** | The fee charged to the payer. | [optional]
**masked_account_number** | **string** | The masked credit card number or account number used by the payer. | [optional]
**comments** | **string** | Comments left by the payer at the initial creation of the transaction. | [optional]
**original_transaction_id** | **int** | The ID of the original transaction. Only present on returns, refunds and similarly derivative transactions. | [optional]
**events** | [**\Tns\\EpayPolicy\Model\TransactionEventModel[]**](TransactionEventModel.md) | A collection of all events that have occurred. | [optional]
**attribute_values** | [**\Tns\\EpayPolicy\Model\AttributeValueModel[]**](AttributeValueModel.md) | A collection of key/value pairs for any custom attribute values for this transaction. | [optional]
**attachments** | [**\Tns\\EpayPolicy\Model\AttachmentModel[]**](AttachmentModel.md) | A collection of all attachments for this transaction. | [optional]
**paid_invoices** | [**\Tns\\EpayPolicy\Model\PaidInvoiceModel[]**](PaidInvoiceModel.md) | A collection of all paid invoices for this transaction. | [optional]
**financing_account** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
