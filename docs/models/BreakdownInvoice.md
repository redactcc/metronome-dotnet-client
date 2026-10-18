# Org.OpenAPITools.Model.BreakdownInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**CustomerId** | **Guid** |  | 
**CreditType** | [**CreditType**](CreditType.md) |  | 
**LineItems** | [**List&lt;InvoiceLineItem&gt;**](InvoiceLineItem.md) |  | 
**Status** | **string** |  | 
**Total** | **decimal** |  | 
**Type** | **string** |  | 
**BreakdownStartTimestamp** | **DateTime** |  | 
**BreakdownEndTimestamp** | **DateTime** |  | 
**CustomerCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetPaymentTermsDays** | **decimal** |  | [optional] 
**StartTimestamp** | **DateTime** | Beginning of the usage period this invoice covers (UTC) | [optional] 
**EndTimestamp** | **DateTime** | End of the usage period this invoice covers (UTC) | [optional] 
**IssuedAt** | **DateTime** | When the invoice was issued (UTC) | [optional] 
**CreatedAt** | **DateTime** | When the invoice was created (UTC). This field is present for correction invoices only. | [optional] 
**ExternalInvoice** | [**ExternalInvoice**](ExternalInvoice.md) |  | [optional] 
**RevenueSystemInvoices** | [**List&lt;RevenueSystemInvoice&gt;**](RevenueSystemInvoice.md) |  | [optional] 
**ContractId** | **Guid** |  | [optional] 
**ContractCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**AmendmentId** | **Guid** |  | [optional] 
**CorrectionRecord** | [**InvoiceCorrectionRecord**](InvoiceCorrectionRecord.md) |  | [optional] 
**ResellerRoyalty** | [**InvoiceResellerRoyalty**](InvoiceResellerRoyalty.md) |  | [optional] 
**CustomFields** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**BillableStatus** | **BillableStatus** |  | [optional] 
**ConstituentInvoices** | [**List&lt;InvoiceConstituentInvoicesInner&gt;**](InvoiceConstituentInvoicesInner.md) | Required on invoices with type USAGE_CONSOLIDATED. List of constituent invoices that were consolidated to create this invoice. | [optional] 
**Payer** | [**InvoicePayer**](InvoicePayer.md) |  | [optional] 
**RegeneratedFromInvoiceId** | **Guid** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

