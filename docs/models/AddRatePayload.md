# Org.OpenAPITools.Model.AddRatePayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RateCardId** | **Guid** | ID of the rate card to update | 
**ProductId** | **Guid** | ID of the product to add a rate for | 
**StartingAt** | **DateTime** | inclusive effective date | 
**Entitled** | **bool** |  | 
**RateType** | **string** |  | 
**PricingGroupValues** | **Dictionary&lt;string, string&gt;** | Optional. List of pricing group key value pairs which will be used to calculate the price. | [optional] 
**BillingFrequency** | **string** | Optional. Frequency to bill subscriptions with. Required for subscription type products with Flat rate. | [optional] 
**EndingBefore** | **DateTime** | exclusive end date | [optional] 
**Price** | **decimal** | Default price. For FLAT and SUBSCRIPTION rate_type, this must be &gt;&#x3D;0. For PERCENTAGE rate_type, this is a decimal fraction, e.g. use 0.1 for 10%; this must be &gt;&#x3D;0 and &lt;&#x3D;1. | [optional] 
**CreditTypeId** | **Guid** | The Metronome ID of the credit type to associate with price, defaults to USD (cents) if not passed. Used by all rate_types except type PERCENTAGE. PERCENTAGE rates use the credit type of associated rates. | [optional] 
**Quantity** | **decimal** | Default quantity. For SUBSCRIPTION rate_type, this must be &gt;&#x3D;0. | [optional] 
**IsProrated** | **bool** | Default proration configuration. Only valid for SUBSCRIPTION rate_type. Must be set to true. | [optional] 
**Tiers** | [**List&lt;Tier&gt;**](Tier.md) | Only set for TIERED rate_type. | [optional] 
**MinimumConfig** | [**MinimumConfig**](MinimumConfig.md) |  | [optional] 
**CustomRate** | **Dictionary&lt;string, Object&gt;** | Only set for CUSTOM rate_type. This field is interpreted by custom rate processors. | [optional] 
**CommitRate** | [**CommitRate**](CommitRate.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

