# Org.OpenAPITools.Model.CreditSubscriptionConfig
The subscription configuration for this credit, if it was generated from a recurring credit with a subscription attached.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SubscriptionId** | **Guid** |  | [optional] 
**Allocation** | **SubscriptionConfigAllocation** |  | [optional] 
**ApplySeatIncreaseConfig** | [**ApplySeatIncreaseConfigForRecurringCommit**](ApplySeatIncreaseConfigForRecurringCommit.md) |  | [optional] 
**AccessPolicy** | **string** | Controls when a customer can access this credit when the attached subscription is payment-gated. &#x60;BILLING_PERIOD_PAID&#x60; releases the credit after payment for its billing period. &#x60;INITIAL_BILLING_PERIOD_PAID_ONLY&#x60; releases the credit after the first payment. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

