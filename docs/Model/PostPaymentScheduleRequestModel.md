# # PostPaymentScheduleRequestModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payer** | **string** | Name of the payer that is shown on the receipt. |
**email_address** | **string** | The recipient of the emailed receipt. |
**token_id** | **string** | The token Id that represents the payment method to be used on the schedule. |
**amount** | **float** | The amount of each recurring payment. |
**start_date** | **\DateTime** | The date of the initial payment. If no date is set, the first payment will be run immediately. | [optional]
**end_date** | **\DateTime** | The date of the last payment if the schedule is supposed to have an end date. | [optional]
**number_of_total_payments** | **int** | The number of payments to process on the schedule if the schedule is only supposed to have a pre-determined number of payments. | [optional]
**interval** | **string** | The interval by which the payments should be run. |
**interval_count** | **int** | The number of days, weeks, etc to wait between payments. |
**attribute_values** | **array<string,string>** | Dictionary of custom attribute values. The key in the dictionary is the identifier of the custom attribute. | [optional]
**comments** | **string** | Comments that are shown on the receipt. | [optional]
**initiating_party_fee** | **float** | The fee being charged by the initiating party of this transaction. This does not include the standard transaction fees. | [optional]
**ip_address** | **string** | The IP Address of the payer. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
