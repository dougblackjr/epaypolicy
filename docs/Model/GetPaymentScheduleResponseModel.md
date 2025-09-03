# # GetPaymentScheduleResponseModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The public Id of the payment schedule. | [optional]
**payer** | **string** | Name of the payer that is shown on the receipt. | [optional]
**email_address** | **string** | The recipient of the emailed receipt. | [optional]
**token_id** | **string** | The token Id that represents the payment method to be used on the schedule. | [optional]
**number_of_total_payments** | **int** | The number of payments to process on the schedule if the payment schedule has a pre-determined list of payments. | [optional]
**number_of_executed_payments** | **int** | The number of executed payments. | [optional]
**amount** | **float** | The amount of each recurring payment. | [optional]
**payer_fee** | **float** | Used if the calling application has pre-calculated a payer fee. In that case, the fee will not be re-calculated. This amount, if set, will not be added to the amount field prior to processing. | [optional]
**start_date** | **\DateTime** | The date of the initial payment. | [optional]
**end_date** | **\DateTime** | The end date of the schedule if the schedule was created with a pre-determined end date. | [optional]
**next_payment_date** | **\DateTime** | The date of the next payment. | [optional]
**interval** | **string** | The interval by which the payments should be run. | [optional]
**interval_count** | **int** | The number of days, weeks, etc to wait between payments. | [optional]
**attribute_values** | **array<string,string>** | Dictionary of custom attribute values. The key in the dictionary is the identifier of the custom attribute. | [optional]
**comments** | **string** | Comments that are shown on the receipt. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
