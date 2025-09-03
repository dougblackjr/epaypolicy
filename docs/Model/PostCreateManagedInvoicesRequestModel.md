# # PostCreateManagedInvoicesRequestModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**policy_number** | **string** |  | [optional]
**effective_date** | **\DateTime** |  | [optional]
**expiration_date** | **\DateTime** |  | [optional]
**payer** | **string** |  |
**email_address** | **string** |  |
**amount** | **float** |  |
**customer_name** | **string** |  |
**invoice_number** | **string** |  |
**due_date** | **\DateTime** |  |
**line_items** | [**\Tns\EpayPolicy\Model\QuoteInvoiceLineItem[]**](QuoteInvoiceLineItem.md) |  |
**taxes** | [**\Tns\EpayPolicy\Model\QuoteInvoiceLineItem[]**](QuoteInvoiceLineItem.md) |  | [optional]
**fees** | [**\Tns\EpayPolicy\Model\QuoteInvoiceLineItem[]**](QuoteInvoiceLineItem.md) |  | [optional]
**show_breakdown_during_payment** | **bool** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
