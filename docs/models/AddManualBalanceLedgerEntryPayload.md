# Org.OpenAPITools.Model.AddManualBalanceLedgerEntryPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose balance is to be updated. | 
**Id** | **Guid** | ID of the balance (commit or credit) to update. | 
**SegmentId** | **Guid** | ID of the segment to update. | 
**Amount** | **decimal** | Amount to add to the segment. A negative number will draw down from the balance. | 
**Reason** | **string** | Reason for the manual adjustment. This will be displayed in the ledger. | 
**ContractId** | **Guid** | ID of the contract to update. Leave blank to update a customer level balance. | [optional] 
**PerGroupAmounts** | **Dictionary&lt;string, decimal&gt;** | If using individually configured commits/credits attached to seat managed subscriptions, the amount to add for each seat. Must sum to total amount. | [optional] 
**Timestamp** | **DateTime** | RFC 3339 timestamp indicating when the manual adjustment takes place. If not provided, it will default to the start of the segment. | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

