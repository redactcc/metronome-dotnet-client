# Org.OpenAPITools.Model.SpendThresholdConfigurationV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsEnabled** | **bool** | When set to false, the contract will not be evaluated against the threshold_amount. Toggling to true will result an immediate evaluation, regardless of prior state. | 
**ThresholdAmount** | **decimal** | Specify the threshold amount for the contract. Each time the contract&#39;s usage hits this amount, a threshold charge will be initiated. | 
**Commit** | [**SpendThresholdCommit**](SpendThresholdCommit.md) |  | 
**PaymentGateConfig** | [**PaymentGateConfigV2**](PaymentGateConfigV2.md) |  | 
**DiscountConfiguration** | [**DiscountConfiguration**](DiscountConfiguration.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

