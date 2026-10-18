# Org.OpenAPITools.Model.ListContractsNamedSchedulesPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer to list contract named schedules for | 
**ContractId** | **Guid** | Optional ID of a contract to scope the results to a single contract | [optional] 
**ScheduleName** | **string** | Optional filter to scope the results to a single schedule name | [optional] 
**Properties** | **Dictionary&lt;string, string&gt;** | Optional key-value filters. A schedule matches when it contains at least this subset of properties. | [optional] 
**CoveringDate** | **DateTime** | If provided, result contains at most one segment covering this date for each schedule. | [optional] 
**Limit** | **int** | Maximum number of named schedules to return. | [optional] 
**NextPage** | **string** | Cursor for pagination. Use the value from a previous response&#39;s next_page. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

