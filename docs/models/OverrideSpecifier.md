# Org.OpenAPITools.Model.OverrideSpecifier

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **Guid** |  | [optional] 
**ProductTags** | **List&lt;string&gt;** |  | [optional] 
**PricingGroupValues** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**PresentationGroupValues** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**CommitIds** | **List&lt;string&gt;** |  | [optional] 
**RecurringCommitIds** | **List&lt;string&gt;** |  | [optional] 
**AnyCommitOrCreditIds** | **List&lt;string&gt;** |  | [optional] 
**BillingFrequency** | **string** |  | [optional] 
**Exclude** | [**List&lt;ExcludeSpecifier&gt;**](ExcludeSpecifier.md) | If provided, the specifier will not apply to product usage that matches the inclusion criteria and any of the excluding values. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

