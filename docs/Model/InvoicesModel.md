# # InvoicesModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payer_name** | **string** |  | [optional]
**email_addresses** | **string[]** |  | [optional]
**auto_pay_subscription_id** | **int** |  | [optional]
**enable_autopay** | **bool** |  | [optional]
**enable_autopay_payless_enrollment** | **bool** |  | [optional]
**auto_pay_email_offset** | **int** |  | [optional]
**auto_pay_cancelable** | **bool** |  | [optional]
**invoice_attribute_metadata** | [**\Tns\EpayPolicy\Model\AttributeMetadataModel[]**](AttributeMetadataModel.md) | Metadata on any custom attributes that will be displayed at the invoice level. | [optional]
**invoices** | [**\Tns\EpayPolicy\Model\InvoiceModel[]**](InvoiceModel.md) | The collection of invoices. | [optional]
**status** | **string** | Whether the referenced account was found. | [optional]
**exception** | [**\Tns\EpayPolicy\Model\SerializableException**](SerializableException.md) |  | [optional]
**any_financing_eligible** | **bool** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
