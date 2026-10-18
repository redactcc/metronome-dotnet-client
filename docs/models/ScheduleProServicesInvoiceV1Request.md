# Org.OpenAPITools.Model.ScheduleProServicesInvoiceV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**ContractId** | **Guid** |  | 
**IssuedAt** | **DateTime** | The date the invoice is issued | 
**LineItems** | [**List&lt;ProServiceInvoiceLineItem&gt;**](ProServiceInvoiceLineItem.md) | Each line requires an amount or both unit_price and quantity. | 
**NetsuiteInvoiceHeaderStart** | **DateTime** | The start date of the invoice header in Netsuite | [optional] 
**NetsuiteInvoiceHeaderEnd** | **DateTime** | The end date of the invoice header in Netsuite | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

