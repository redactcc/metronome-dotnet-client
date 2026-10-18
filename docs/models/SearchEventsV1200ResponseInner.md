# Org.OpenAPITools.Model.SearchEventsV1200ResponseInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**CustomerId** | **string** | The ID of the customer in the ingest event body | 
**EventType** | **string** |  | 
**Timestamp** | **DateTime** |  | 
**TransactionId** | **string** |  | 
**Properties** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**IsDuplicate** | **bool** |  | [optional] 
**ProcessedAt** | **DateTime** |  | [optional] 
**MatchedCustomer** | [**SearchEventsV1200ResponseInnerMatchedCustomer**](SearchEventsV1200ResponseInnerMatchedCustomer.md) |  | [optional] 
**MatchedBillableMetrics** | [**List&lt;BillableMetricForEventsSearch&gt;**](BillableMetricForEventsSearch.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

