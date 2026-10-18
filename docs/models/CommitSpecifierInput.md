# Org.OpenAPITools.Model.CommitSpecifierInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **Guid** | If provided, the specifier will only apply to the product with the specified ID. | [optional] 
**ProductTags** | **List&lt;string&gt;** | If provided, the specifier will only apply to products with all the specified tags. | [optional] 
**PricingGroupValues** | **Dictionary&lt;string, string&gt;** | If provided, the specifier will apply to product usage with these set of pricing group values. | [optional] 
**PresentationGroupValues** | **Dictionary&lt;string, string&gt;** | If provided, the specifier will apply to product usage with these set of presentation group values. | [optional] 
**Exclude** | [**List&lt;ExcludeSpecifier&gt;**](ExcludeSpecifier.md) | If provided, the specifier will not apply to product usage that matches the inclusion criteria and any of the excluding values. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

