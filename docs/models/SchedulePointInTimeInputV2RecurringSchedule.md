# Org.OpenAPITools.Model.SchedulePointInTimeInputV2RecurringSchedule
Enter the unit price and quantity for the charge or instead only send the amount. If amount is sent, the unit price is assumed to be the amount and quantity is inferred to be 1.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StartingAt** | **DateTime** | RFC 3339 timestamp (inclusive). | 
**EndingBefore** | **DateTime** | RFC 3339 timestamp (exclusive). | 
**Frequency** | **RecurringScheduleFrequencyV2** |  | 
**AmountDistribution** | **string** |  | 
**UnitPrice** | **decimal** | Unit price for the charge. Will be multiplied by quantity to determine the amount and must be specified with quantity. If specified amount cannot be provided. | [optional] 
**Quantity** | **decimal** | Quantity for the charge. Will be multiplied by unit_price to determine the amount and must be specified with unit_price. If specified amount cannot be provided. | [optional] 
**Amount** | **decimal** | Amount for the charge. Can be provided instead of unit_price and quantity. If amount is sent, the unit_price is assumed to be the amount and quantity is inferred to be 1. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

