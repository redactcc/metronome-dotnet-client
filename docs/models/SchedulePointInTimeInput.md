# Org.OpenAPITools.Model.SchedulePointInTimeInput
Must provide either schedule_items or recurring_schedule.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreditTypeId** | **Guid** | Defaults to USD (cents) if not passed. | [optional] 
**ScheduleItems** | [**List&lt;SchedulePointInTimeInputScheduleItemsInner&gt;**](SchedulePointInTimeInputScheduleItemsInner.md) | Either provide amount or provide both unit_price and quantity. | [optional] 
**RecurringSchedule** | [**SchedulePointInTimeInputRecurringSchedule**](SchedulePointInTimeInputRecurringSchedule.md) |  | [optional] 
**DoNotInvoice** | **bool** | This field is only applicable to commit invoice schedules. If true, this schedule will not generate an invoice. | [optional] [default to false]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

