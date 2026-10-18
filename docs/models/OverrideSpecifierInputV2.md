# Org.OpenAPITools.Model.OverrideSpecifierInputV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CommitIds** | **List&lt;string&gt;** | If provided, the override will only apply to the specified commits. Can only be used for commit specific overrides. If not provided, the override will apply to all commits. | [optional] 
**RecurringCommitIds** | **List&lt;string&gt;** | Can only be used for commit specific overrides. Must be used in conjunction with one of product_id, product_tags, pricing_group_values, or presentation_group_values. If provided, the override will only apply to commits created by the specified recurring commit ids. | [optional] 
**AnyCommitOrCreditIds** | **List&lt;string&gt;** | Can only be used for commit specific overrides. Must be used in conjunction with one of &#x60;product_id&#x60;, &#x60;product_tags&#x60;, &#x60;pricing_group_values&#x60;, or &#x60;presentation_group_values&#x60;. Must be used instead of both &#x60;commit_ids&#x60; and &#x60;recurring_commit_ids&#x60; If provided, the override will apply to any specified commit, credit, recurring commit or recurring credit IDs. | [optional] 
**ProductId** | **Guid** | If provided, the override will only apply to the product with the specified ID. | [optional] 
**ProductTags** | **List&lt;string&gt;** | If provided, the override will only apply to products with all the specified tags. | [optional] 
**PricingGroupValues** | **Dictionary&lt;string, string&gt;** | A map of pricing group names to values. The override will only apply to products with the specified pricing group values. | [optional] 
**PresentationGroupValues** | **Dictionary&lt;string, string&gt;** | A map of group names to values. The override will only apply to line items with the specified presentation group values. Can only be used for multiplier overrides. | [optional] 
**BillingFrequency** | **string** |  | [optional] 
**Exclude** | [**List&lt;ExcludeSpecifier&gt;**](ExcludeSpecifier.md) | If provided, the specifier will not apply to product usage that matches the inclusion criteria and any of the excluding values. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

