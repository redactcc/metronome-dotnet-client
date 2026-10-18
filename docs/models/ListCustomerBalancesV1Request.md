# Org.OpenAPITools.Model.ListCustomerBalancesV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**Id** | **Guid** |  | [optional] 
**AccessType** | **string** | Filters balances by how they are drawn down. &#x60;SPEND&#x60; deducts the dollar cost of usage. &#x60;QUANTITY&#x60; deducts the number of units used. | [optional] 
**CoveringDate** | **DateTime** | Return only balances that have access schedules that \&quot;cover\&quot; the provided date | [optional] 
**StartingAt** | **DateTime** | Include only balances that have any access on or after the provided date | [optional] 
**EffectiveBefore** | **DateTime** | Include only balances that have any access before the provided date (exclusive) | [optional] 
**IncludeContractBalances** | **bool** | Include balances on the contract level. | [optional] 
**IncludeArchived** | **bool** | Include archived credits and credits from archived contracts. | [optional] 
**IncludeLedgers** | **bool** | Include ledgers in the response. Setting this flag may cause the query to be slower. | [optional] 
**IncludeBalance** | **bool** | Include the balance of credits and commits in the response. Setting this flag may cause the query to be slower. | [optional] 
**NextPage** | **string** | The next page token from a previous response. | [optional] 
**Limit** | **int** | The maximum number of commits to return. Defaults to 25. | [optional] [default to 25]
**ExcludeZeroBalances** | **bool** | Exclude balances with zero amounts from the response. | [optional] 
**WebhookNotificationId** | **string** | Indicates that this API request was triggered by a webhook notification with the provided ID. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

