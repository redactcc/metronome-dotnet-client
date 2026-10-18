# Org.OpenAPITools.Model.GetContractV2Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**ContractId** | **Guid** |  | 
**IncludeLedgers** | **bool** | Include commit/credit ledgers in the response. Setting this flag may cause the query to be slower. Cannot be used with as_of_date parameter. | [optional] 
**AsOfDate** | **DateTime** | Optional RFC 3339 timestamp. Return the contract as of this date. Cannot be used with include_ledgers parameter. | [optional] 
**IncludeBalance** | **bool** | Include the balance of credits and commits in the response. Setting this flag may cause the query to be slower. | [optional] 
**WebhookNotificationId** | **string** | Indicates that this API request was triggered by a webhook notification with the provided ID. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

