# Org.OpenAPITools.Model.CommitRate
A distinct rate on the rate card. You can choose to use this rate rather than list rate when consuming a credit or commit.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RateType** | **string** |  | 
**Price** | **decimal** | Commit rate price. For FLAT rate_type, this must be &gt;&#x3D;0. For PERCENTAGE rate_type, this is a decimal fraction, e.g. use 0.1 for 10%; this must be &gt;&#x3D;0 and &lt;&#x3D;1. | [optional] 
**Tiers** | [**List&lt;Tier&gt;**](Tier.md) | Only set for TIERED rate_type. | [optional] 
**MinimumConfig** | [**MinimumConfig**](MinimumConfig.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

