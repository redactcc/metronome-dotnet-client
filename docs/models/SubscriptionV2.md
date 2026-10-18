# Org.OpenAPITools.Model.SubscriptionV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SubscriptionRate** | [**SubscriptionRate**](SubscriptionRate.md) |  | 
**CollectionSchedule** | **string** |  | 
**Proration** | [**SubscriptionProrationV2**](SubscriptionProrationV2.md) |  | 
**QuantitySchedule** | [**List&lt;SubscriptionQuantitySchedule&gt;**](SubscriptionQuantitySchedule.md) | List of quantity schedule items for the subscription. Only includes the current quantity and future quantity changes. | 
**BillingPeriods** | [**SubscriptionBillingPeriods**](SubscriptionBillingPeriods.md) |  | 
**QuantityManagementMode** | **string** | Determines how the subscription&#39;s quantity is controlled. Defaults to QUANTITY_ONLY. **QUANTITY_ONLY**: The subscription quantity is specified directly on the subscription. &#x60;initial_quantity&#x60; must be provided with this option. Compatible with recurring commits/credits that use POOLED allocation. **SEAT_BASED**: Use when you want to pass specific seat identifiers (e.g. add user_123) to increment and decrement a subscription quantity, rather than directly providing the quantity. You must use a **SEAT_BASED** subscription to use a linked recurring credit with an allocation per seat. &#x60;seat_config&#x60; must be provided with this option. | 
**CreatedAt** | **DateTime** |  | 
**StartingAt** | **DateTime** |  | 
**Id** | **Guid** |  | [optional] 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**SeatConfig** | [**SubscriptionSeatConfig**](SubscriptionSeatConfig.md) |  | [optional] 
**EndingBefore** | **DateTime** |  | [optional] 
**FiatCreditTypeId** | **Guid** |  | [optional] 
**CustomCreditTypeId** | **Guid** | If provided, the subscription&#39;s price will be in terms of this custom pricing unit instead of the fiat currency. | [optional] 
**BillingCycleConfig** | [**SubscriptionBillingCycleConfig**](SubscriptionBillingCycleConfig.md) |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**ProductCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**Status** | **string** |  | [optional] 
**PaidQuantity** | **decimal** |  | [optional] 
**PaymentGateConfig** | [**SubscriptionPaymentGateConfig**](SubscriptionPaymentGateConfig.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

