# Org.OpenAPITools.Model.ExternalInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillingProviderType** | **BillingProviderType** |  | 
**InvoiceId** | **string** |  | [optional] 
**IssuedAtTimestamp** | **DateTime** |  | [optional] 
**ExternalStatus** | **ExternalInvoiceStatus** |  | [optional] 
**PdfUrl** | **string** | A URL to the PDF of the invoice, if available from the billing provider. | [optional] 
**Tax** | [**ExternalInvoiceTax**](ExternalInvoiceTax.md) |  | [optional] 
**InvoicedTotal** | **decimal** | The total amount invoiced, if available from the billing provider. | [optional] 
**InvoicedSubTotal** | **decimal** | The subtotal amount invoiced, if available from the billing provider. | [optional] 
**BillingProviderError** | **string** | Error message from the billing provider, if available. | [optional] 
**ExternalPaymentId** | **string** | The ID of the payment in the external system, if available. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

