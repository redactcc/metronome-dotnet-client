# Org.OpenAPITools.Model.ListCustomerCommitsV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**CommitId** | **Guid** |  | [optional] 
**AccessType** | **string** | Filters commits by how their balances are drawn down. &#x60;SPEND&#x60; deducts the dollar cost of usage. &#x60;QUANTITY&#x60; deducts the number of units used. | [optional] 
**CoveringDate** | **DateTime** | Include only commits that have access schedules that \&quot;cover\&quot; the provided date | [optional] 
**StartingAt** | **DateTime** | Include only commits that have any access on or after the provided date | [optional] 
**EffectiveBefore** | **DateTime** | Include only commits that have any access before the provided date (exclusive) | [optional] 
**IncludeContractCommits** | **bool** | Include commits on the contract level. | [optional] 
**IncludeArchived** | **bool** | Include archived commits and commits from archived contracts. | [optional] 
**IncludeLedgers** | **bool** | Include commit ledgers in the response. Setting this flag may cause the query to be slower. | [optional] 
**IncludeBalance** | **bool** | Include the balance in the response. Setting this flag may cause the query to be slower. | [optional] 
**NextPage** | **string** | The next page token from a previous response. | [optional] 
**Limit** | **int** | The maximum number of commits to return. Defaults to 25. | [optional] [default to 25]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

