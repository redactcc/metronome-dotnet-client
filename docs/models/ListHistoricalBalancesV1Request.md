# Org.OpenAPITools.Model.ListHistoricalBalancesV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**ContractId** | **Guid** | Return only historical balances from this contract. | [optional] 
**Id** | **Guid** | Return only the historical balance with this ID. | [optional] 
**CoveringDate** | **DateTime** | Return only historical balances with access schedules that cover this date. | [optional] 
**StartingAt** | **DateTime** | Return only historical balances with any access on or after this date. | [optional] 
**EffectiveBefore** | **DateTime** | Return only historical balances with any access before this date (exclusive). | [optional] 
**RetiredAfter** | **DateTime** | Return only balances that became historical at or after this date. | [optional] 
**RetiredBefore** | **DateTime** | Return only balances that became historical before this date (exclusive). | [optional] 
**IncludeLedgers** | **bool** | Include ledgers in the response. Setting this flag may cause the query to be slower. | [optional] [default to false]
**NextPage** | **string** | The next page token from a previous response. | [optional] 
**Limit** | **int** | The maximum number of historical balances to return. Defaults to 25. | [optional] [default to 25]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

