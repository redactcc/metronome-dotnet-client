# Org.OpenAPITools.Model.PrepaidRechargeGrantOptionsStripeOptions
Options for prepaid credits using Stripe

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CalculateTax** | **bool** | Whether to calculate tax for the prepaid invoice Defaults to false if not provided. | [optional] 
**TaxPlatform** | **TaxPlatform** |  | [optional] 
**SkipTaxOnTaxPlatformError** | **bool** | Whether to skip tax calculation if the tax platform returns an error. Defaults to true if not provided. | [optional] 
**TaxProductId** | **string** | Optional Stripe product ID to use for the tax line item. If omitted a random Stripe product will be created and used for the invoice. | [optional] 
**RedirectUrl** | **string** | The URL to redirect the user to after they have corrected a billing issue | [optional] 
**InvoiceCustomFields** | [**List&lt;NameValuePair&gt;**](NameValuePair.md) | Custom fields to add to the prepaid invoice | [optional] 
**InvoiceMetadata** | **Dictionary&lt;string, Object&gt;** | Invoice metadata to add to the prepaid invoice | [optional] 
**PaymentMethodId** | **string** | Optional Stripe payment method ID to use. | [optional] 
**ProductId** | **string** | Optional Stripe product ID to use for the grant. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

