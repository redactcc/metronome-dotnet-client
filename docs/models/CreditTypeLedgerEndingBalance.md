# Org.OpenAPITools.Model.CreditTypeLedgerEndingBalance
the effective balances at the end of the specified time window

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExcludingPending** | **decimal** | the ending balance, including the balance of all grants that have not expired before the effective_at date and deductions that happened before the effective_at date | 
**IncludingPending** | **decimal** | the excluding_pending balance plus any pending invoice deductions and expirations that will happen by the effective_at date | 
**EffectiveAt** | **DateTime** | the ending_before request parameter (if supplied) or the current billing period&#39;s end date | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

