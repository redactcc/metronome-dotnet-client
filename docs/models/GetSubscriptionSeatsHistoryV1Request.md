# Org.OpenAPITools.Model.GetSubscriptionSeatsHistoryV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**ContractId** | **Guid** |  | 
**SubscriptionId** | **Guid** |  | 
**Limit** | **int** | Maximum number of seat schedule entries to return. Defaults to 10. Required range: 1 &lt;&#x3D; x &lt;&#x3D; 10. | [optional] [default to 10]
**Cursor** | **string** | Cursor for pagination. Use the value from the &#x60;next_page&#x60; field of the previous response to retrieve the next page of results. | [optional] 
**CoveringDate** | **DateTime** | Get the seats history segment for the covering date. Cannot be used with &#x60;starting_at&#x60; or &#x60;ending_before&#x60;. | [optional] 
**StartingAt** | **DateTime** | Include seats history segments that are active at or after this timestamp. Use with &#x60;ending_before&#x60; to get a specific time range. If not set, there&#39;s no lower bound. | [optional] 
**EndingBefore** | **DateTime** | Include seats history segments that are active at or before this timestamp. Use with &#x60;starting_at&#x60; to get a specific time range. If not set, there&#39;s no upper bound. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

