# Org.OpenAPITools.Model.OverwriteRateInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RateType** | **string** |  | 
**Price** | **decimal** | Default price. For FLAT rate_type, this must be &gt;&#x3D;0. For PERCENTAGE rate_type, this is a decimal fraction, e.g. use 0.1 for 10%; this must be &gt;&#x3D;0 and &lt;&#x3D;1. | [optional] 
**Quantity** | **decimal** | Default quantity. For SUBSCRIPTION rate_type, this must be &gt;&#x3D;0. | [optional] 
**IsProrated** | **bool** | Default proration configuration. Only valid for SUBSCRIPTION rate_type. Must be set to true. | [optional] 
**Tiers** | [**List&lt;Tier&gt;**](Tier.md) | Only set for TIERED rate_type. | [optional] 
**MinimumConfig** | [**MinimumConfig**](MinimumConfig.md) |  | [optional] 
**CustomRate** | **Dictionary&lt;string, Object&gt;** | Only set for CUSTOM rate_type. This field is interpreted by custom rate processors. | [optional] 
**CreditTypeId** | **Guid** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

