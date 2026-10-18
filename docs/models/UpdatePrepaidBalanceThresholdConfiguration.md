# Org.OpenAPITools.Model.UpdatePrepaidBalanceThresholdConfiguration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsEnabled** | **bool** | When set to false, the contract will not be evaluated against the threshold_amount. Toggling to true will result an immediate evaluation, regardless of prior state. | [optional] 
**ThresholdAmount** | **decimal** | Specify the threshold amount for the contract. Each time the contract&#39;s balance lowers to this amount, a threshold charge will be initiated. | [optional] 
**RechargeToAmount** | **decimal** | Specify the amount the balance should be recharged to. | [optional] 
**CustomCreditTypeId** | **Guid** | If provided, the threshold, recharge-to amount, and the resulting threshold commit amount will be in terms of this credit type instead of the fiat currency. | [optional] 
**Commit** | [**UpdatePrepaidBalanceThresholdCommit**](UpdatePrepaidBalanceThresholdCommit.md) |  | [optional] 
**PaymentGateConfig** | [**PaymentGateConfigV2**](PaymentGateConfigV2.md) |  | [optional] 
**DiscountConfiguration** | [**UpdateDiscountConfiguration**](UpdateDiscountConfiguration.md) |  | [optional] 
**ThresholdBalanceSpecifiers** | [**List&lt;ThresholdBalanceSpecifierV2&gt;**](ThresholdBalanceSpecifierV2.md) | Determines which balances are excluded from remaining balance calculation for threshold billing. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

