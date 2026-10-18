# Org.OpenAPITools.Model.GetContractNamedSchedulePayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose named schedule is to be retrieved | 
**ContractId** | **Guid** | ID of the contract whose named schedule is to be retrieved | 
**ScheduleName** | **string** | The identifier for the schedule to be retrieved | 
**CoveringDate** | **DateTime** | If provided, at most one schedule segment will be returned (the one that covers this date). If not provided, all segments will be returned. | [optional] 
**Properties** | **Dictionary&lt;string, string&gt;** | A set of key-value pairs that qualifies which schedule should be applied when looking up a schedule by name. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

