# Org.OpenAPITools.Model.BillableMetricBase

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Id** | **Guid** |  | 
**GroupBy** | **List&lt;string&gt;** | (DEPRECATED) use group_keys instead | [optional] 
**GroupKeys** | **List&lt;List&lt;string&gt;&gt;** | Property names that are used to group usage costs on an invoice. Each entry represents a set of properties used to slice events into distinct buckets. | [optional] 
**Aggregate** | **string** | (DEPRECATED) use aggregation_type instead | [optional] 
**AggregateKeys** | **List&lt;string&gt;** | (DEPRECATED) use aggregation_key instead | [optional] 
**Filter** | **Dictionary&lt;string, Object&gt;** | (DEPRECATED) use property_filters &amp; event_type_filter instead | [optional] 
**AggregationKey** | **string** | A key that specifies which property of the event is used to aggregate data. This key must be one of the property filter names and is not applicable when the aggregation type is &#39;count&#39;. | [optional] 
**EventTypeFilter** | [**EventTypeFilter**](EventTypeFilter.md) |  | [optional] 
**PropertyFilters** | [**List&lt;PropertyFilter&gt;**](PropertyFilter.md) | A list of filters to match events to this billable metric. Each filter defines a rule on an event property. All rules must pass for the event to match the billable metric. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**Sql** | **string** | The SQL query associated with the billable metric | [optional] 
**ArchivedAt** | **DateTime** | RFC 3339 timestamp indicating when the billable metric was archived. If not provided, the billable metric is not archived. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

