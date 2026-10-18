# Org.OpenAPITools.Model.PreviewEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventType** | **string** |  | 
**Timestamp** | **string** | RFC 3339 formatted. If not provided, the current time will be used. | [optional] 
**Properties** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**TransactionId** | **string** | Optional unique identifier for event deduplication. When provided, preview events are automatically deduplicated against historical events from the past 34 days.  Duplicate transaction IDs within the same request will return an error.  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

