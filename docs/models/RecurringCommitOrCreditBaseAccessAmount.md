# Org.OpenAPITools.Model.RecurringCommitOrCreditBaseAccessAmount
The amount of commit to grant.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UnitPrice** | **decimal** |  | 
**CreditTypeId** | **Guid** | This ID identifies the credit type for the access amount. Quantity-based recurring commits and credits return the null credit type UUID. | 
**AccessType** | **string** | Indicates how the balance of child commits is drawn down. &#x60;SPEND&#x60; deducts the dollar cost of usage. &#x60;QUANTITY&#x60; deducts the number of units used. | [optional] 
**Quantity** | **decimal** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

