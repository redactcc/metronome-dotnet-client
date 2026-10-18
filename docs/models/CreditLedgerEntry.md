# Org.OpenAPITools.Model.CreditLedgerEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **decimal** | an amount representing the change to the customer&#39;s credit balance | 
**Reason** | **string** |  | 
**RunningBalance** | **decimal** | the running balance for this credit type at the time of the ledger entry, including all preceding charges | 
**EffectiveAt** | **DateTime** |  | 
**CreatedBy** | **string** |  | 
**CreditGrantId** | **Guid** | the credit grant this entry is related to | 
**InvoiceId** | **Guid** | if this entry is a deduction, the Metronome ID of the invoice where the credit deduction was consumed; if this entry is a grant, the Metronome ID of the invoice where the grant&#39;s paid_amount was charged | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

