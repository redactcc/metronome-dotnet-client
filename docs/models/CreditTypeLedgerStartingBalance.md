# Org.OpenAPITools.Model.CreditTypeLedgerStartingBalance

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExcludingPending** | **decimal** | the starting balance, including all posted grants, deductions, and expirations that happened at or before the effective_at timestamp | 
**IncludingPending** | **decimal** | the excluding_pending balance plus any pending activity that has not been posted at the time of the query | 
**EffectiveAt** | **DateTime** | the starting_on request parameter (if supplied) or the first credit grant&#39;s effective_at date | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

