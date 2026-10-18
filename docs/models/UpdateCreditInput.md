# Org.OpenAPITools.Model.UpdateCreditInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreditId** | **Guid** |  | 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**AccessSchedule** | [**UpdateAccessScheduleInput**](UpdateAccessScheduleInput.md) |  | [optional] 
**RolloverFraction** | **decimal** |  | [optional] 
**NetsuiteSalesOrderId** | **string** |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the credit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the credit applies to all products. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the credit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the credit applies to all products. | [optional] 
**ProductId** | **Guid** |  | [optional] 
**Priority** | **decimal** |  | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 
**RateType** | **string** | If provided, updates the credit to use the specified rate type for current and future invoices. Previously finalized invoices will need to be voided and regenerated to reflect the rate type change. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

