# Org.OpenAPITools.Model.ListCustomerCreditsV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**CreditId** | **Guid** |  | [optional] 
**CoveringDate** | **DateTime** | Return only credits that have access schedules that \&quot;cover\&quot; the provided date | [optional] 
**StartingAt** | **DateTime** | Include only credits that have any access on or after the provided date | [optional] 
**EffectiveBefore** | **DateTime** | Include only credits that have any access before the provided date (exclusive) | [optional] 
**IncludeContractCredits** | **bool** | Include credits on the contract level. | [optional] 
**IncludeArchived** | **bool** | Include archived credits and credits from archived contracts. | [optional] 
**IncludeLedgers** | **bool** | Include credit ledgers in the response. Setting this flag may cause the query to be slower. | [optional] 
**IncludeBalance** | **bool** | Include the balance in the response. Setting this flag may cause the query to be slower. | [optional] 
**NextPage** | **string** | The next page token from a previous response. | [optional] 
**Limit** | **int** | The maximum number of commits to return. Defaults to 25. | [optional] [default to 25]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

