# Org.OpenAPITools.Model.CommitUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**AccessSchedule** | [**AccessScheduleUpdate**](AccessScheduleUpdate.md) |  | [optional] 
**NetsuiteSalesOrderId** | **string** |  | [optional] 
**RolloverFraction** | **decimal** |  | [optional] 
**InvoiceSchedule** | [**InvoiceScheduleUpdate**](InvoiceScheduleUpdate.md) |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**Specifiers** | [**List&lt;CommitSpecifierInput&gt;**](CommitSpecifierInput.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. This field cannot be used together with &#x60;applicable_product_ids&#x60; or &#x60;applicable_product_tags&#x60;. Instead, to target usage by product or product tag, pass those values in the body of &#x60;specifiers&#x60;. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ProductId** | **Guid** |  | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 
**Priority** | **decimal** | If multiple commits are applicable, the one with the lower priority will apply first. | [optional] 
**RateType** | **string** | If set, the commit&#39;s rate type was updated to the specified value. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

