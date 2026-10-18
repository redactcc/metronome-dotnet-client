# Org.OpenAPITools.Model.RateSchedule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **Guid** |  | 
**ProductName** | **string** |  | 
**ProductTags** | **List&lt;string&gt;** |  | 
**ProductCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | 
**StartingAt** | **DateTime** |  | 
**Entitled** | **bool** |  | 
**Rate** | [**Rate**](Rate.md) |  | 
**PricingGroupValues** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**EndingBefore** | **DateTime** |  | [optional] 
**CommitRate** | [**CommitRate**](CommitRate.md) |  | [optional] 
**BillingFrequency** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

