# Org.OpenAPITools.Model.EditCommitPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose commit is being edited | 
**CommitId** | **Guid** | ID of the commit to edit | 
**Name** | **string** | Updated name for the commit | [optional] 
**Description** | **string** | Updated description for the commit | [optional] 
**AccessSchedule** | [**UpdateAccessScheduleInput**](UpdateAccessScheduleInput.md) |  | [optional] 
**InvoiceSchedule** | [**UpdateInvoiceScheduleInput**](UpdateInvoiceScheduleInput.md) |  | [optional] 
**InvoiceContractId** | **Guid** | ID of contract to use for invoicing | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ApplicableContractIds** | **List&lt;Guid&gt;** | Which contracts the customer-level commit applies to. If set to null, the commit applies to all of the customer&#39;s contracts. This field cannot be edited for POSTPAID commits or contract-level commits. | [optional] 
**Specifiers** | [**List&lt;CommitSpecifierInput&gt;**](CommitSpecifierInput.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. This field cannot be used together with &#x60;applicable_product_ids&#x60; or &#x60;applicable_product_tags&#x60;. Instead, to target usage by product or product tag, pass those values in the body of &#x60;specifiers&#x60;. | [optional] 
**ProductId** | **Guid** |  | [optional] 
**Priority** | **decimal** | If multiple commits are applicable, the one with the lower priority will apply first. | [optional] 
**RateType** | **string** | If provided, updates the commit to use the specified rate type for current and future invoices. Previously finalized invoices will need to be voided and regenerated to reflect the rate type change. | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

