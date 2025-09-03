# # GetManagedInvoiceResponseModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**public_id** | **string** | The Public identifier of the managed invoice. | [optional]
**account_name** | **string** | The name of the account. | [optional]
**payer** | **string** | The name of the payer. | [optional]
**create_date** | **\DateTime** | The date when invoice was created. | [optional]
**created_by_user** | **string** | The user who created the invoice. | [optional]
**due_date** | **\DateTime** | The expiration date. | [optional]
**status** | **string** | Represents the current status of the invoice. | [optional]
**invoice_total** | **float** | The sum of all charges specified on invoice. | [optional]
**cancel_date** | **\DateTime** | The date when invoice was cancelled or voided. | [optional]
**complete_date** | **\DateTime** | The date when invoice was completed or paid. | [optional]
**off_platform_date** | **\DateTime** | The date when invoice was completed or paid Offplatform. | [optional]
**quick_quote_date** | **\DateTime** | The date when quick quote was retrieved to check for financing. | [optional]
**email_send_date** | **\DateTime** | The date when an email was sent to the payer. | [optional]
**line_items** | [**\Tns\EpayPolicy\Model\QuoteInvoiceLineItem[]**](QuoteInvoiceLineItem.md) |  | [optional]
**taxes** | [**\Tns\EpayPolicy\Model\QuoteInvoiceLineItem[]**](QuoteInvoiceLineItem.md) |  | [optional]
**fees** | [**\Tns\EpayPolicy\Model\QuoteInvoiceLineItem[]**](QuoteInvoiceLineItem.md) |  | [optional]
**financing_info** | [**\Tns\EpayPolicy\Model\QuoteInvoiceFinancingInfoModel**](QuoteInvoiceFinancingInfoModel.md) |  | [optional]
**quick_quote** | [**\Tns\EpayPolicy\Model\QuickQuoteModel**](QuickQuoteModel.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
