# Org.OpenAPITools.Model.PaymentGateConfigV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PaymentGateType** | **string** | Gate access to the commit balance based on successful collection of payment. Select STRIPE for Metronome to facilitate payment via Stripe. Select EXTERNAL to facilitate payment using your own payment integration. Select NONE if you do not wish to payment gate the commit balance. | 
**TaxType** | **string** | Stripe tax is only supported for Stripe payment gateway. Select NONE if you do not wish  Metronome to calculate tax on your behalf. Leaving this field blank will default to NONE. | [optional] 
**StripeConfig** | [**PaymentGateConfigV2StripeConfig**](PaymentGateConfigV2StripeConfig.md) |  | [optional] 
**PrecalculatedTaxConfig** | [**PaymentGateConfigPrecalculatedTaxConfig**](PaymentGateConfigPrecalculatedTaxConfig.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

