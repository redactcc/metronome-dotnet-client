# Org.OpenAPITools.Model.ListContractsV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**IncludeLedgers** | **bool** | Include commit ledgers in the response. Setting this flag may cause the query to be slower. | [optional] 
**IncludeBalance** | **bool** | Include the balance of credits and commits in the response. Setting this flag may cause the query to be slower. | [optional] 
**IncludeArchived** | **bool** | Include archived contracts in the response | [optional] 
**StartingAt** | **DateTime** | Optional RFC 3339 timestamp. If provided, the response will include only contracts where starting_at is on or after the provided date.  This cannot be provided if the covering_date filter is provided. | [optional] 
**CoveringDate** | **DateTime** | Optional RFC 3339 timestamp. If provided, the response will include only contracts effective on the provided date.  This cannot be provided if the starting_at filter is provided. | [optional] 
**Limit** | **int** | Max number of contracts to return per page. Range: 1-20. Default: 20. | [optional] 
**Cursor** | **string** | Cursor from a previous response to fetch the next page of contracts. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

