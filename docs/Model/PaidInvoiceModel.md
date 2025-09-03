# # PaidInvoiceModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier for the invoice. | [optional]
**paid_amount** | **float** | The amount being paid on the given invoice. | [optional]
**finance_down_payment** | **float** | The amount of financed down payment for the given invoice | [optional]
**financed_amount** | **float** | The amount of the invoice that has been financed. | [optional]
**comment** | **string** | Comments by the payer for the paid invoice. | [optional]
**division** | **string** | Division for routing funds. | [optional]
**due_date** | **\DateTime** | Date Invoice is Due. | [optional]
**attribute_values** | **array<string,string>** | Attribute values to be saved with the paid invoice. This is used by the payment page. | [optional]
**search_attribute_values** | **array<string,string>** | Attribute values to locate this invoice in its management system. | [optional]
**managed_invoice_id** | **int** | Managed Invoice Id. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
