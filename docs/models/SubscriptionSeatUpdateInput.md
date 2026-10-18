# Org.OpenAPITools.Model.SubscriptionSeatUpdateInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AddSeatIds** | [**List&lt;SubscriptionSeatUpdateAssignedSeat&gt;**](SubscriptionSeatUpdateAssignedSeat.md) | Adds seat IDs to the subscription.  If there are unassigned seats, the new seat IDs will fill these unassigned seats and not increase the total subscription quantity. Otherwise, if there are more new seat IDs than unassigned seats, the total subscription quantity will increase. | [optional] 
**RemoveSeatIds** | [**List&lt;SubscriptionSeatUpdateAssignedSeat&gt;**](SubscriptionSeatUpdateAssignedSeat.md) | Removes seat IDs from the subscription, if possible.  If a seat ID is removed, the total subscription quantity will decrease. Otherwise, if the seat ID is not found on the subscription, this is a no-op. | [optional] 
**AddUnassignedSeats** | [**List&lt;SubscriptionSeatUpdateUnassignedSeat&gt;**](SubscriptionSeatUpdateUnassignedSeat.md) | Adds unassigned seats to the subscription. This will increase the total subscription quantity. | [optional] 
**RemoveUnassignedSeats** | [**List&lt;SubscriptionSeatUpdateUnassignedSeat&gt;**](SubscriptionSeatUpdateUnassignedSeat.md) | Removes unassigned seats from the subscription. This will decrease the total subscription quantity if there are are unassigned seats. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

