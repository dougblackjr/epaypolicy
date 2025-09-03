# # InvoiceModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier of the invoice. |
**name** | **string** | The customer name on the invoice. |
**due_date** | **\DateTime** | The due date of the invoice. |
**amount** | **float** | The total amount due. | [optional]
**maximum_amount** | **float** | The maximum amount the payer is allowed to pay. | [optional]
**minimum_amount** | **float** | The minimum amount the payer is allowed to pay. | [optional]
**allow_partial_payment** | **bool** | Indicates whether a partial payment is allowed on the invoice. | [optional]
**comment** | **string** | The Comment for the Invoice submitted by the payer. | [optional]
**division_id** | **string** | Optional division id to specify recieving account. | [optional]
**down_payment_amount** | **float** | If finance eligible, the required down payment | [optional]
**number_of_installments** | **int** | If financed, the number of installment payments. | [optional]
**installment_amount** | **float** | if financed, the amount of each installment payment. | [optional]
**attribute_values** | [**\Tns\\EpayPolicy\Model\AttributeValueModel[]**](AttributeValueModel.md) | The actual values of the custom attributes at the invoice level. |
**search_attribute_values** | **array<string,string>** | Attributes used to find this invoice in management system | [optional]
**invoice_items** | [**\Tns\\EpayPolicy\Model\InvoiceItemModel[]**](InvoiceItemModel.md) | A collection of invoice items. |
**policy_effective_date** | **\DateTime** | Effective date of the policy. | [optional]
**policy_number** | **string** | The policy number. | [optional]
**is_financing_eligible** | **bool** |  | [optional] [readonly]
**finance_status_description** | **string** |  | [optional]
**finance_eligibility_hash** | **string** |  | [optional]
**data_token** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
