# Org.OpenAPITools.Model.PackageSubscriptionCustomization

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TemplateSubscriptionId** | **Guid** | ID of the template subscription on the package to customize. Provide exactly one of template_subscription_id or subscription_alias. | [optional] 
**SubscriptionAlias** | **string** | Human-readable alias of the template subscription on the package to customize, as an alternative to template_subscription_id. Provide exactly one of the two. | [optional] 
**InitialQuantity** | **decimal** | The initial quantity for the subscription. Must be a non-negative value. Provide for a QUANTITY_ONLY subscription. | [optional] 
**InitialSeatIds** | **List&lt;string&gt;** | Seat identifiers to assign at the start of a SEAT_BASED subscription. | [optional] 
**InitialUnassignedSeats** | **decimal** | Number of unassigned seats to provision at the start of a SEAT_BASED subscription. | [optional] 
**SubscriptionAnchorDate** | **DateTime** | Billing cycle anchor date for this subscription, required when the template&#39;s billing_cycle_anchor is CUSTOM_DATE and disallowed otherwise. Must be on or before the subscription&#39;s starting_at. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

