# Org.OpenAPITools.Model.CreditTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Product** | [**SubscriptionRateProduct**](SubscriptionRateProduct.md) |  | 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**Priority** | **decimal** |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** |  | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** |  | [optional] 
**Specifiers** | [**List&lt;CommitSpecifier&gt;**](CommitSpecifier.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. | [optional] 
**AccessSchedule** | [**RelativeScheduleDuration**](RelativeScheduleDuration.md) |  | [optional] 
**RateType** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

