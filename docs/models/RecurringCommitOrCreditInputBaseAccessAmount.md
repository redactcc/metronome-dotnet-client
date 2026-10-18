# Org.OpenAPITools.Model.RecurringCommitOrCreditInputBaseAccessAmount
The amount of commit to grant.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UnitPrice** | **decimal** |  | 
**AccessType** | **string** | Indicates how the balance of child commits is drawn down. &#x60;SPEND&#x60; deducts the dollar cost of usage. &#x60;QUANTITY&#x60; deducts the number of units used. | [optional] 
**Quantity** | **decimal** | This field is required unless a subscription is attached via &#x60;subscription_config&#x60;. | [optional] 
**CreditTypeId** | **Guid** | Defaults to USD (cents) if not passed | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

