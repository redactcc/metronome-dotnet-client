# Org.OpenAPITools.Model.UpdateCommitInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CommitId** | **Guid** |  | 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**AccessSchedule** | [**UpdateAccessScheduleInput**](UpdateAccessScheduleInput.md) |  | [optional] 
**NetsuiteSalesOrderId** | **string** |  | [optional] 
**RolloverFraction** | **decimal** |  | [optional] 
**InvoiceSchedule** | [**UpdateInvoiceScheduleInput**](UpdateInvoiceScheduleInput.md) |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ProductId** | **Guid** |  | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 
**Priority** | **decimal** |  | [optional] 
**RateType** | **string** | If provided, updates the commit to use the specified rate type for current and future invoices. Previously finalized invoices will need to be voided and regenerated to reflect the rate type change. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

