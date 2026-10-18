# Org.OpenAPITools.Model.UpdateSpendThresholdConfiguration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsEnabled** | **bool** | When set to false, the contract will not be evaluated against the threshold_amount. Toggling to true will result an immediate evaluation, regardless of prior state. | [optional] 
**ThresholdAmount** | **decimal** | Specify the threshold amount for the contract. Each time the contract&#39;s usage hits this amount, a threshold charge will be initiated. | [optional] 
**Commit** | [**UpdateSpendThresholdCommit**](UpdateSpendThresholdCommit.md) |  | [optional] 
**PaymentGateConfig** | [**PaymentGateConfigV2**](PaymentGateConfigV2.md) |  | [optional] 
**DiscountConfiguration** | [**UpdateDiscountConfiguration**](UpdateDiscountConfiguration.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

