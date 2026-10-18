# Org.OpenAPITools.Model.ListContractsV2Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**IncludeLedgers** | **bool** | Include commit/credit ledgers in the response. Setting this flag may cause the response to be slower. | [optional] 
**IncludeArchived** | **bool** | Include archived contracts in the response. | [optional] 
**IncludeBalance** | **bool** | Include the balance of credits and commits in the response. Setting this flag may cause the response to be slower. | [optional] 
**StartingAt** | **DateTime** | Optional RFC 3339 timestamp. Only include contracts that started on or after this date. This cannot be provided if covering_date filter is provided. | [optional] 
**CoveringDate** | **DateTime** | Optional RFC 3339 timestamp. Only include contracts active on the provided date. This cannot be provided if starting_at filter is provided. | [optional] 
**Limit** | **decimal** | Max number of contracts to return per page. Range: 1-20. Default: 20. | [optional] 
**Cursor** | **string** | Cursor from a previous response to fetch the next page of contracts. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

