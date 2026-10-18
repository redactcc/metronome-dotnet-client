# Org.OpenAPITools.Model.PrepaidBalanceThresholdCommit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **string** | The commit product that will be used to generate the line item for commit payment. | 
**Name** | **string** | Specify the name of the line item for the threshold charge. If left blank, it will default to the commit product name. | [optional] 
**Description** | **string** |  | [optional] 
**Priority** | **decimal** | The priority of the commit, used to determine drawdown order. Lower priority commits are consumed first. Defaults to 100 if not specified. | [optional] 
**Duration** | [**RelativeDate**](RelativeDate.md) |  | [optional] 
**RolloverFraction** | **decimal** | Fraction of the created commit&#39;s unused balance that will roll over. Must be between 0 and 1. | [optional] 
**RateType** | **string** | Whether the created commits will be charged at commit rate or list rate. | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the threshold commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the threshold commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**Specifiers** | [**List&lt;CommitSpecifierInput&gt;**](CommitSpecifierInput.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. This field cannot be used together with &#x60;applicable_product_ids&#x60; or &#x60;applicable_product_tags&#x60;. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

