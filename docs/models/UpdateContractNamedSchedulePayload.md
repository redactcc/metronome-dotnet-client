# Org.OpenAPITools.Model.UpdateContractNamedSchedulePayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose named schedule is to be updated | 
**ContractId** | **Guid** | ID of the contract whose named schedule is to be updated | 
**ScheduleName** | **string** | The identifier for the schedule to be updated | 
**StartingAt** | **DateTime** |  | 
**EndingBefore** | **DateTime** |  | [optional] 
**Value** | **Object** | The value to set for the named schedule. The structure of this object is specific to the named schedule. | 
**Properties** | **Dictionary&lt;string, string&gt;** | A set of key-value pairs that qualifies which schedule should be applied when looking up a schedule by name. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

