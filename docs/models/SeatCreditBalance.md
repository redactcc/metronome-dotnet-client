# Org.OpenAPITools.Model.SeatCreditBalance

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The credit ID | 
**Balance** | **decimal** | The current balance for this credit for this specific seat | 
**StartDate** | **DateTime** | The datetime when the credit becomes active | 
**AccessType** | **string** | Indicates how the balance is drawn down. &#x60;SPEND&#x60; deducts the dollar cost of usage. &#x60;QUANTITY&#x60; deducts the number of units used. | [optional] 
**CreditTypeId** | **Guid** | The credit type for this credit. Quantity-based credits return the null credit type UUID. | [optional] 
**EndDate** | **DateTime** | The datetime when the credit expires | [optional] 
**LedgerEntries** | [**List&lt;SeatBalanceCreditLedger&gt;**](SeatBalanceCreditLedger.md) | Transaction history for this credit for this seat (only included if include_ledgers&#x3D;true) | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

