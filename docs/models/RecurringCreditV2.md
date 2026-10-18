# Org.OpenAPITools.Model.RecurringCreditV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Product** | [**SubscriptionRateProduct**](SubscriptionRateProduct.md) |  | 
**AccessAmount** | [**RecurringCommitOrCreditBaseAccessAmount**](RecurringCommitOrCreditBaseAccessAmount.md) |  | 
**Priority** | **decimal** | Will be passed down to the individual commits | 
**RateType** | **string** | Whether the created commits will use the commit rate or list rate | 
**StartingAt** | **DateTime** | Determines the start time for the first commit | 
**CommitDuration** | [**RecurringCommitOrCreditBaseCommitDuration**](RecurringCommitOrCreditBaseCommitDuration.md) |  | 
**AnchorDate** | **DateTime** | The date this recurring commit&#39;s billing periods are anchored to. | 
**Contract** | [**VoidInvoiceV1200ResponseData**](VoidInvoiceV1200ResponseData.md) |  | [optional] 
**Name** | **string** | Displayed on invoices. Will be passed through to the individual commits | [optional] 
**Description** | **string** | Will be passed down to the individual commits | [optional] 
**RolloverFraction** | **decimal** | Will be passed down to the individual commits. This controls how much of an individual unexpired commit will roll over upon contract transition. Must be between 0 and 1. | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Will be passed down to the individual commits | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Will be passed down to the individual commits | [optional] 
**Specifiers** | [**List&lt;CommitSpecifier&gt;**](CommitSpecifier.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. | [optional] 
**NetsuiteSalesOrderId** | **string** | Will be passed down to the individual commits | [optional] 
**EndingBefore** | **DateTime** | Determines when the contract will stop creating recurring commits. Optional | [optional] 
**RecurrenceFrequency** | **string** | The frequency at which the recurring commits will be created. If not provided: - The commits will be created on the usage invoice frequency. If provided: - The period defined in the duration will correspond to this frequency. - Commits will be created aligned with the recurring commit&#39;s starting_at rather than the usage invoice dates. - Daily recurring commits have a limit of one per contract, and are unable to be created with seat-based subscriptions | [optional] 
**Proration** | **string** | Determines whether the first and last commit will be prorated. If not provided, the default is FIRST_AND_LAST (i.e. prorate both the first and last commits). | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 
**SubscriptionConfig** | [**RecurringCommitSubscriptionConfig**](RecurringCommitSubscriptionConfig.md) |  | [optional] 
**ProrationRounding** | [**RecurringCreditV2AllOfProrationRounding**](RecurringCreditV2AllOfProrationRounding.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

