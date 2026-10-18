# Org.OpenAPITools.Model.UpdateRecurringCommitInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RecurringCommitId** | **Guid** |  | 
**AccessAmount** | [**RecurringCommitOrCreditUpdateBaseAccessAmount**](RecurringCommitOrCreditUpdateBaseAccessAmount.md) |  | [optional] 
**InvoiceAmount** | [**RecurringCommitOrCreditUpdateBaseAccessAmount**](RecurringCommitOrCreditUpdateBaseAccessAmount.md) |  | [optional] 
**EndingBefore** | **DateTime** |  | [optional] 
**RateType** | **string** | If provided, updates the recurring commit to use the specified rate type when generating future commits. | [optional] 
**ProrationRounding** | [**UpdateRecurringCommitInputProrationRounding**](UpdateRecurringCommitInputProrationRounding.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

