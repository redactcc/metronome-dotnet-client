# Org.OpenAPITools.Model.PagedUsageAggregate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StartingOn** | **DateTime** |  | 
**EndingBefore** | **DateTime** |  | 
**GroupKey** | **string** | Use &#x60;group&#x60; instead. The group key for single-key grouping. | 
**GroupValue** | **string** | Use &#x60;group&#x60; instead. The group value for single-key grouping. | 
**Group** | **Dictionary&lt;string, string&gt;** | Map of group key to their value for this usage aggregate. For simple group keys, this should be a single key e.g. &#x60;{\&quot;region\&quot;: \&quot;US-East\&quot;}&#x60; For compound group keys, this should contain the values of each group key that forms the compound e.g. &#x60;{\&quot;region\&quot;: \&quot;US-East\&quot;, \&quot;team\&quot;: \&quot;engineering\&quot;}&#x60;  | [optional] 
**Value** | **decimal** |  | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

