# Org.OpenAPITools.Model.UpdateSubscriptionInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SubscriptionId** | **Guid** |  | 
**Name** | **string** |  | [optional] 
**EndingBefore** | **DateTime** |  | [optional] 
**QuantityManagementModeUpdate** | [**UpdateSubscriptionInputQuantityManagementModeUpdate**](UpdateSubscriptionInputQuantityManagementModeUpdate.md) |  | [optional] 
**QuantityUpdates** | [**List&lt;UpdateSubscriptionInputQuantityUpdatesInner&gt;**](UpdateSubscriptionInputQuantityUpdatesInner.md) | Quantity changes are applied on the effective date based on the order which they are sent. For example, if I scheduled the quantity to be 12 on May 21 and then scheduled a quantity delta change of -1, the result from that day would be 11. | [optional] 
**SeatUpdates** | [**SubscriptionSeatUpdateInput**](SubscriptionSeatUpdateInput.md) |  | [optional] 
**ProrationRounding** | [**NullableProrationRoundingConfig**](NullableProrationRoundingConfig.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

