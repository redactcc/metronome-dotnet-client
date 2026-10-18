# Org.OpenAPITools.Model.MoveToHistoryResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**HistoricalCount** | **decimal** | Number of commits successfully moved to historical in this request | 
**HistoricalCommitIds** | **List&lt;Guid&gt;** | IDs of the commits that were moved to historical | 
**SkippedCount** | **decimal** | Number of commits that were skipped due to ineligibility | 
**SkippedReasons** | [**List&lt;MoveToHistoryResponseSkippedReasonsInner&gt;**](MoveToHistoryResponseSkippedReasonsInner.md) | Per-commit details on why specific commits were not moved to historical | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

