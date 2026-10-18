# Org.OpenAPITools.Model.ContractHierarchyConfigurationInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Parent** | [**ContractParentHierarchyConfigurationInput**](ContractParentHierarchyConfigurationInput.md) |  | [optional] 
**Payer** | **string** | Indicates which customer should pay for the child&#39;s invoice charges  **SELF**: The child pays for its own invoice charges  **PARENT**: The parent pays for the child&#39;s invoice charges | [optional] 
**UsageStatementBehavior** | **string** | Indicates the behavior of the child&#39;s invoice statements on the parent&#39;s invoices.  **CONSOLIDATE**: Child&#39;s invoice statements will be added to parent&#39;s consolidated invoices  **SEPARATE**: Child&#39;s invoice statements will appear not appear on parent&#39;s consolidated invoices | [optional] 
**ParentBehavior** | [**ContractHierarchyConfigurationInputParentBehavior**](ContractHierarchyConfigurationInputParentBehavior.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

