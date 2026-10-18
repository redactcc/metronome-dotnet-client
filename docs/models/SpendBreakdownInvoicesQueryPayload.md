# Org.OpenAPITools.Model.SpendBreakdownInvoicesQueryPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StartingOn** | **DateTime** | RFC 3339 timestamp. Breakdowns will only be returned for time windows that start on or after this time. | 
**EndingBefore** | **DateTime** | RFC 3339 timestamp. Breakdowns will only be returned for time windows that end on or before this time. | 
**SkipZeroQtyLineItems** | **bool** | If set, all zero quantity line items will be filtered out of the response. | [optional] 
**CreditTypeId** | **Guid** | If provided, only invoices with the specified credit type id will be included in the response. | [optional] 
**Sort** | **string** | Invoice sort order by issued_at, e.g. date_asc or date_desc.  Defaults to date_asc. | [optional] [default to SortEnum.DateAsc]
**WindowSize** | **string** | The granularity of the breakdowns to return. Defaults to \&quot;day\&quot;. | [optional] 
**GroupKeys** | **List&lt;string&gt;** | A list of keys that can be used to additionally segment the values of the billable metric when making usage queries. Must be valid keys that are present in the billable metrics or an empty list. The value will be ignored and the default keys will be used if: billable metric is MAX type; product uses tiered pricing model; product has quantity rounding enabled; there are contract overrides based on presentation group keys  | [optional] 
**GroupFilters** | **Dictionary&lt;string, List&lt;string&gt;&gt;** | An object where the keys are the group keys and the values are arrays of group values. If the values is an empty array, the returned usage data will be aggregated across all values for that key. The value will be ignored and the default keys will be used if: billable metric is MAX type; product uses tiered pricing model; product has quantity rounding enabled; there are contract overrides based on presentation group keys  | [optional] 
**Limit** | **int** | Max number of results that should be returned. For daily and \&quot;none\&quot; breakdowns, the response can return up to 35 days worth of breakdowns. If there are more results, a cursor to the next page is returned. | [optional] [default to 100]
**NextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

