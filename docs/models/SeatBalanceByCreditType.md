# Org.OpenAPITools.Model.SeatBalanceByCreditType

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreditTypeId** | **Guid** | This ID identifies the credit type for the balance. Quantity-based balances return the null credit type UUID. | 
**Balance** | **decimal** | The total balance across all commits and credits for this seat, of this credit type. | 
**StartingBalance** | **decimal** | The total initial balances of all commits and credits for this seat, of this credit type. | 
**AccessType** | **string** | Indicates how the balance is drawn down. &#x60;SPEND&#x60; deducts the dollar cost of usage. &#x60;QUANTITY&#x60; deducts the number of units used. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

