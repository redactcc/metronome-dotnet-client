# Org.OpenAPITools.Model.RateSelectorWithProductTags

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillingFrequency** | **string** | Subscription rates matching the billing frequency will be included in the response. | [optional] 
**ProductId** | **Guid** | Rates matching the product id will be included in the response. | [optional] 
**ProductTags** | **List&lt;string&gt;** | List of product tags, rates matching any of the tags will be included in the response. | [optional] 
**PricingGroupValues** | **Dictionary&lt;string, string&gt;** | List of pricing group key value pairs, rates matching all of the key / value pairs will be included in the response. | [optional] 
**PartialPricingGroupValues** | **Dictionary&lt;string, string&gt;** | List of pricing group key value pairs, rates containing the matching key / value pairs will be included in the response. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

