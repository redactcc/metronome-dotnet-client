# Org.OpenAPITools.Model.SeatCommitBalance

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The commit or credit ID | 
**Balance** | **decimal** | The current balance for this commit for this specific seat | 
**StartDate** | **DateTime** | The datetime when the commit becomes active | 
**AccessType** | **string** | Indicates how the balance is drawn down. &#x60;SPEND&#x60; deducts the dollar cost of usage. &#x60;QUANTITY&#x60; deducts the number of units used. | [optional] 
**CreditTypeId** | **Guid** | The credit type for this commit. Quantity-based commits return the null credit type UUID. | [optional] 
**EndDate** | **DateTime** | The datetime when the commit expires | [optional] 
**LedgerEntries** | [**List&lt;SeatBalanceCommitLedger&gt;**](SeatBalanceCommitLedger.md) | Transaction history for this commit for this seat (only included if include_ledgers&#x3D;true) | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

