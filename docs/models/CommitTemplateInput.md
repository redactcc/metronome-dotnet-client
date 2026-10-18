# Org.OpenAPITools.Model.CommitTemplateInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**ProductId** | **Guid** |  | 
**AccessSchedule** | [**RelativeScheduleDurationInput**](RelativeScheduleDurationInput.md) |  | 
**RateType** | **string** |  | [optional] 
**Name** | **string** | displayed on invoices | [optional] 
**InvoiceSchedule** | [**CommitTemplateInputInvoiceSchedule**](CommitTemplateInputInvoiceSchedule.md) |  | [optional] 
**Description** | **string** | Used only in UI/API. It is not exposed to end customers. | [optional] 
**RolloverFraction** | **decimal** | Fraction of unused segments that will be rolled over. Must be between 0 and 1. | [optional] 
**Priority** | **decimal** | If multiple commits are applicable, the one with the lower priority will apply first. | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**Specifiers** | [**List&lt;CommitSpecifierInput&gt;**](CommitSpecifierInput.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. This field cannot be used together with &#x60;applicable_product_ids&#x60; or &#x60;applicable_product_tags&#x60;. | [optional] 
**TemporaryId** | **string** | A temporary ID for the commit that can be used to reference the commit for commit specific overrides. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

