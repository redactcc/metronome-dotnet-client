# Org.OpenAPITools.Model.ResellerRoyaltyOrUpdateInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ResellerType** | **ResellerType** |  | 
**Fraction** | **decimal** |  | [optional] 
**NetsuiteResellerId** | **string** |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Must provide at least one of applicable_product_ids or applicable_product_tags. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Must provide at least one of applicable_product_ids or applicable_product_tags. | [optional] 
**StartingAt** | **DateTime** |  | [optional] 
**EndingBefore** | **DateTime** | Use null to indicate that the existing end timestamp should be removed. | [optional] 
**ResellerContractValue** | **decimal** |  | [optional] 
**AwsOptions** | [**InvoiceResellerRoyaltyAwsOptions**](InvoiceResellerRoyaltyAwsOptions.md) |  | [optional] 
**GcpOptions** | [**InvoiceResellerRoyaltyGcpOptions**](InvoiceResellerRoyaltyGcpOptions.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

