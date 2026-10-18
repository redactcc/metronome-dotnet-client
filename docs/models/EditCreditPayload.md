# Org.OpenAPITools.Model.EditCreditPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose credit is being edited | 
**CreditId** | **Guid** | ID of the credit to edit | 
**Name** | **string** | Updated name for the credit | [optional] 
**Description** | **string** | Updated description for the credit | [optional] 
**AccessSchedule** | [**UpdateAccessScheduleInput**](UpdateAccessScheduleInput.md) |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the credit applies to. If both applicable_product_ids and applicable_product_tags are not provided, the credit applies to all products. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the credit applies to. If both applicable_product_ids and applicable_product_tags are not provided, the credit applies to all products. | [optional] 
**ApplicableContractIds** | **List&lt;Guid&gt;** | Which contracts the customer-level credit applies to. If set to null, the credit applies to all of the customer&#39;s contracts. This field cannot be set on a contract-level credit. | [optional] 
**Specifiers** | [**List&lt;CommitSpecifierInput&gt;**](CommitSpecifierInput.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. This field cannot be used together with &#x60;applicable_product_ids&#x60; or &#x60;applicable_product_tags&#x60;. Instead, to target usage by product or product tag, pass those values in the body of &#x60;specifiers&#x60;. | [optional] 
**ProductId** | **Guid** |  | [optional] 
**Priority** | **decimal** | If multiple commits are applicable, the one with the lower priority will apply first. | [optional] 
**RateType** | **string** | If provided, updates the credit to use the specified rate type for current and future invoices. Previously finalized invoices will need to be voided and regenerated to reflect the rate type change. | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

