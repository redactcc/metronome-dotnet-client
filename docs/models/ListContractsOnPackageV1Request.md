# Org.OpenAPITools.Model.ListContractsOnPackageV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PackageId** | **Guid** |  | 
**StartingAt** | **DateTime** | Optional RFC 3339 timestamp. Only include contracts that started on or after this date. This cannot be provided if covering_date filter is provided. | [optional] 
**CoveringDate** | **DateTime** | Optional RFC 3339 timestamp. Only include contracts active on the provided date. This cannot be provided if starting_at filter is provided. | [optional] 
**IncludeArchived** | **bool** | Default false. Determines whether to include archived contracts in the results | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

