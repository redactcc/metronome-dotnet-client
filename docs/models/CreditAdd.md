# Org.OpenAPITools.Model.CreditAdd

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Type** | **string** |  | 
**Product** | [**SubscriptionRateProduct**](SubscriptionRateProduct.md) |  | 
**Name** | **string** |  | [optional] 
**Priority** | **decimal** | If multiple credits or commits are applicable, the one with the lower priority will apply first. | [optional] 
**AccessSchedule** | [**ScheduleDuration**](ScheduleDuration.md) |  | [optional] 
**Description** | **string** |  | [optional] 
**RolloverFraction** | **decimal** |  | [optional] 
**RateType** | **string** |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** |  | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** |  | [optional] 
**Specifiers** | [**List&lt;CommitSpecifierInput&gt;**](CommitSpecifierInput.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. This field cannot be used together with &#x60;applicable_product_ids&#x60; or &#x60;applicable_product_tags&#x60;. Instead, to target usage by product or product tag, pass those values in the body of &#x60;specifiers&#x60;. | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

