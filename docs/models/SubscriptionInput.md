# Org.OpenAPITools.Model.SubscriptionInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SubscriptionRate** | [**SubscriptionRateInput**](SubscriptionRateInput.md) |  | 
**CollectionSchedule** | **string** |  | 
**Proration** | [**SubscriptionProrationInput**](SubscriptionProrationInput.md) |  | 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**InitialQuantity** | **decimal** | The initial quantity for the subscription. It must be non-negative value. Required if quantity_management_mode is QUANTITY_ONLY. | [optional] 
**StartingAt** | **DateTime** | Inclusive start time for the subscription. If not provided, defaults to contract start date | [optional] 
**EndingBefore** | **DateTime** | Exclusive end time for the subscription. If not provided, subscription inherits contract end date. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**TemporaryId** | **string** | A temporary ID used to reference the subscription in recurring commit/credit subscription configs created within the same payload. | [optional] 
**QuantityManagementMode** | **string** | Determines how the subscription&#39;s quantity is controlled. Defaults to QUANTITY_ONLY. **QUANTITY_ONLY**: The subscription quantity is specified directly on the subscription. &#x60;initial_quantity&#x60; must be provided with this option. Compatible with recurring commits/credits that use POOLED allocation. **SEAT_BASED**: Use when you want to pass specific seat identifiers (e.g. add user_123) to increment and decrement a subscription quantity, rather than directly providing the quantity. You must use a **SEAT_BASED** subscription to use a linked recurring credit with an allocation per seat. &#x60;seat_config&#x60; must be provided with this option. | [optional] 
**SeatConfig** | [**SubscriptionSeatConfigInput**](SubscriptionSeatConfigInput.md) |  | [optional] 
**BillingCycleConfig** | [**SubscriptionBillingCycleConfigInput**](SubscriptionBillingCycleConfigInput.md) |  | [optional] 
**PaymentGateConfig** | [**SubscriptionPaymentGateConfigInput**](SubscriptionPaymentGateConfigInput.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

