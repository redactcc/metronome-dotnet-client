# Org.OpenAPITools.Model.HistoricalContractUsageInvoiceInputPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**ContractId** | **Guid** |  | 
**CreditTypeId** | **Guid** |  | 
**InclusiveStartDate** | **DateTime** |  | 
**ExclusiveEndDate** | **DateTime** |  | 
**IssueDate** | **DateTime** |  | 
**UsageLineItems** | [**List&lt;HistoricalContractUsageInvoiceLineItemInput&gt;**](HistoricalContractUsageInvoiceLineItemInput.md) |  | 
**BreakdownGranularity** | **string** |  | [optional] 
**BillableStatus** | **BillableStatus** |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

