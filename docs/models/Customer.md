# Org.OpenAPITools.Model.Customer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | the Metronome ID of the customer | 
**ExternalId** | **string** | (deprecated, use ingest_aliases instead) the first ID (Metronome or ingest alias) that can be used in usage events | 
**IngestAliases** | **List&lt;string&gt;** | aliases for this customer that can be used instead of the Metronome customer ID in usage events | 
**Name** | **string** |  | 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

