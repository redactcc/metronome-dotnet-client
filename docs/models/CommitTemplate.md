# Org.OpenAPITools.Model.CommitTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Type** | **string** |  | 
**Product** | [**SubscriptionRateProduct**](SubscriptionRateProduct.md) |  | 
**RateType** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Priority** | **decimal** | If multiple credits or commits are applicable, the one with the lower priority will apply first. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**AccessSchedule** | [**RelativeScheduleDuration**](RelativeScheduleDuration.md) |  | [optional] 
**InvoiceSchedule** | [**CommitTemplateInvoiceSchedule**](CommitTemplateInvoiceSchedule.md) |  | [optional] 
**Description** | **string** |  | [optional] 
**RolloverFraction** | **decimal** |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** |  | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** |  | [optional] 
**Specifiers** | [**List&lt;CommitSpecifier&gt;**](CommitSpecifier.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

