# Org.OpenAPITools.Model.UpdateSubscriptionInputQuantityUpdatesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StartingAt** | **DateTime** |  | 
**Quantity** | **decimal** | The new quantity for the subscription. Must be provided if quantity_delta is not provided. Must be non-negative. | [optional] 
**QuantityDelta** | **decimal** | The delta to add to the subscription&#39;s quantity. Must be provided if quantity is not provided. Can&#39;t be zero. It also can&#39;t result in a negative quantity on the subscription. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

