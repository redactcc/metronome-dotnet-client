# Org.OpenAPITools.Model.UsageBatchQueryPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**WindowSize** | **string** | A window_size of \&quot;day\&quot; or \&quot;hour\&quot; will return the usage for the specified period segmented into daily or hourly aggregates. A window_size of \&quot;none\&quot; will return a single usage aggregate for the entirety of the specified period. | 
**StartingOn** | **DateTime** | Must be aligned to UTC midnight, e.g. &#x60;2024-01-01T00:00:00Z&#x60;. | 
**EndingBefore** | **DateTime** | Must be aligned to UTC midnight and at least one day after &#x60;starting_on&#x60;. | 
**CustomerIds** | **List&lt;Guid&gt;** | A list of Metronome customer IDs to fetch usage for. If absent, usage for all customers will be returned. | [optional] 
**BillableMetrics** | [**List&lt;UsageBatchQueryPayloadBillableMetricsInner&gt;**](UsageBatchQueryPayloadBillableMetricsInner.md) | A list of billable metrics to fetch usage for. If absent, all billable metrics will be returned. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

