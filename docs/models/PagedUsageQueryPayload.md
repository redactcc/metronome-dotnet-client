# Org.OpenAPITools.Model.PagedUsageQueryPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**BillableMetricId** | **Guid** |  | 
**WindowSize** | **string** | A window_size of \&quot;day\&quot; or \&quot;hour\&quot; will return the usage for the specified period segmented into daily or hourly aggregates. A window_size of \&quot;none\&quot; will return a single usage aggregate for the entirety of the specified period. | 
**StartingOn** | **DateTime** | Must be aligned to UTC midnight, e.g. &#x60;2024-01-01T00:00:00Z&#x60;. | [optional] 
**EndingBefore** | **DateTime** | Must be aligned to UTC midnight and at least one day after &#x60;starting_on&#x60;. | [optional] 
**GroupBy** | [**PagedUsageQueryPayloadGroupBy**](PagedUsageQueryPayloadGroupBy.md) |  | [optional] 
**GroupKey** | **List&lt;string&gt;** | Group key to group usage by. Supports both simple (single key) and compound (multiple keys) group keys.  For simple group keys, provide a single key e.g. &#x60;[\&quot;region\&quot;]&#x60;. For compound group keys, provide multiple keys e.g. &#x60;[\&quot;region\&quot;, \&quot;team\&quot;]&#x60;.  For streaming metrics, the keys must be defined as a simple or compound group key on the billable metric. For compound group keys, all keys must match an exact compound group key definition — partial matches are not allowed.  Cannot be used together with &#x60;group_by&#x60;.  | [optional] 
**GroupFilters** | **Dictionary&lt;string, List&lt;string&gt;&gt;** | Object mapping group keys to arrays of values to filter on. Only usage matching these filter values will be returned. Keys must be present in group_key. Omit a key or use an empty array to include all values for that dimension. The combined number of entries across all value arrays may not exceed 200.  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

