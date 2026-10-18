# Org.OpenAPITools.Model.ProServiceInvoiceLineItem
Describes the line item for a professional service charge on an invoice.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfessionalServiceId** | **Guid** |  | 
**AmendmentId** | **Guid** | If the professional_service_id was added on an amendment, this is required. | [optional] 
**UnitPrice** | **decimal** | If specified, this overrides the unit price on the pro service term. Must also provide quantity (but not amount) if providing unit_price. | [optional] 
**Quantity** | **decimal** | Quantity for the charge. Will be multiplied by unit_price to determine the amount. | [optional] 
**Amount** | **decimal** | Amount for the term on the new invoice. | [optional] 
**NetsuiteInvoiceBillingStart** | **DateTime** | The start date for the billing period on the invoice. | [optional] 
**NetsuiteInvoiceBillingEnd** | **DateTime** | The end date for the billing period on the invoice. | [optional] 
**Metadata** | **string** | For client use. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

