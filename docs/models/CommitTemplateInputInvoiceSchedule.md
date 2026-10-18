# Org.OpenAPITools.Model.CommitTemplateInputInvoiceSchedule
Required for \"POSTPAID\" commits: the true up invoice will be generated at this time and only one schedule item is allowed; the total must match access_schedule amount. Optional for \"PREPAID\" commits: if not provided, this will be a \"complimentary\" commit with no invoice.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ScheduleItems** | [**List&lt;RelativeSchedulePointInTimeInputScheduleItemsInner&gt;**](RelativeSchedulePointInTimeInputScheduleItemsInner.md) | Either provide amount or provide both unit_price and quantity. | 
**CreditTypeId** | **Guid** | Defaults to USD (cents) if not passed. | [optional] 
**DoNotInvoice** | **bool** | If true, this schedule will not generate an invoice. | [optional] [default to false]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

