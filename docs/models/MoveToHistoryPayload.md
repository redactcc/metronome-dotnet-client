# Org.OpenAPITools.Model.MoveToHistoryPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose commits are being moved to historical | 
**ContractId** | **Guid** | ID of the contract containing the commits | 
**CommitIds** | **List&lt;Guid&gt;** | IDs of the commits to move to historical | 
**DryRun** | **bool** | If true, previews which commits would be moved to historical and which would be skipped, without making changes | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

