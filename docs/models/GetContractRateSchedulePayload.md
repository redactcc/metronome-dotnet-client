# Org.OpenAPITools.Model.GetContractRateSchedulePayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer for whose contract to get the rate schedule for. | 
**ContractId** | **Guid** | ID of the contract to get the rate schedule for. | 
**At** | **DateTime** | optional timestamp which overlaps with the returned rate schedule segments. When not specified, the current timestamp will be used. | [optional] 
**Selectors** | [**List&lt;RateSelectorWithProductTags&gt;**](RateSelectorWithProductTags.md) | List of rate selectors, rates matching ANY of the selectors will be included in the response. Passing no selectors will result in all rates being returned. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

