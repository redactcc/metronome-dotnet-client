# Org.OpenAPITools.Model.SpendBreakdownInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**CustomerId** | **Guid** |  | 
**CreditType** | [**CreditType**](CreditType.md) |  | 
**LineItems** | [**List&lt;InvoiceLineItem&gt;**](InvoiceLineItem.md) |  | 
**Status** | **string** |  | 
**Type** | **string** |  | 
**BreakdownStartTimestamp** | **DateTime** |  | 
**BreakdownEndTimestamp** | **DateTime** |  | 
**StartTimestamp** | **DateTime** | Beginning of the usage period this invoice covers (UTC) | [optional] 
**EndTimestamp** | **DateTime** | End of the usage period this invoice covers (UTC) | [optional] 
**IssuedAt** | **DateTime** | When the invoice was issued (UTC) | [optional] 
**CreatedAt** | **DateTime** | When the invoice was created (UTC). This field is present for correction invoices only. | [optional] 
**ContractId** | **Guid** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

