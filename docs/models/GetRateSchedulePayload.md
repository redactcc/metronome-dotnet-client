# Org.OpenAPITools.Model.GetRateSchedulePayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RateCardId** | **Guid** | ID of the rate card to get the schedule for | 
**StartingAt** | **DateTime** | inclusive starting point for the rates schedule | 
**EndingBefore** | **DateTime** | optional exclusive end date for the rates schedule. When not specified rates will show all future schedule segments. | [optional] 
**Selectors** | [**List&lt;RateSelector&gt;**](RateSelector.md) | List of rate selectors, rates matching ANY of the selector will be included in the response Passing no selectors will result in all rates being returned. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

