# Org.OpenAPITools.Model.CommitPaymentGateConfigStripeConfig
Only applicable if using STRIPE as your payment gateway type.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PaymentType** | **string** | If left blank, will default to INVOICE | 
**InvoiceMetadata** | **Dictionary&lt;string, string&gt;** | Metadata to be added to the Stripe invoice. Only applicable if using INVOICE as your payment type. | [optional] 
**OnSessionPayment** | **bool** | If true, the payment will be made assuming the customer is present (i.e. on session).   If false, the payment will be made assuming the customer is not present (i.e. off session).  For cardholders from a country with an e-mandate requirement (e.g. India), the payment may be declined.  If left blank, will default to false. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

