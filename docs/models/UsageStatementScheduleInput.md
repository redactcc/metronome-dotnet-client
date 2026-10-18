# Org.OpenAPITools.Model.UsageStatementScheduleInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Frequency** | **string** |  | 
**Day** | **string** | If not provided, defaults to the first day of the month. | [optional] 
**BillingAnchorDate** | **DateTime** | Required when using CUSTOM_DATE. This option lets you set a historical billing anchor date, aligning future billing cycles with a chosen cadence. For example, if a contract starts on 2024-09-15 and you set the anchor date to 2024-09-10 with a MONTHLY frequency, the first usage statement will cover 09-15 to 10-10. Subsequent statements will follow the 10th of each month. | [optional] 
**InvoiceGenerationStartingAt** | **DateTime** | The date Metronome should start generating usage invoices. If unspecified, contract start date will be used. This is useful to set if you want to import historical invoices via our &#39;Create Historical Invoices&#39; API rather than having Metronome automatically generate them. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

