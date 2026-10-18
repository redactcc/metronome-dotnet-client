# Org.OpenAPITools.Model.RecurringCommitOrCreditTemplateBase

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Product** | [**SubscriptionRateProduct**](SubscriptionRateProduct.md) |  | 
**AccessAmount** | [**RecurringCommitOrCreditBaseAccessAmount**](RecurringCommitOrCreditBaseAccessAmount.md) |  | 
**Priority** | **decimal** |  | 
**RateType** | **string** | Whether the created commits will use the commit rate or list rate | 
**StartingAtOffset** | [**RelativeDate**](RelativeDate.md) |  | 
**CommitDuration** | [**RecurringCommitOrCreditTemplateBaseCommitDuration**](RecurringCommitOrCreditTemplateBaseCommitDuration.md) |  | 
**Name** | **string** |  | [optional] 
**Description** | **string** |  | [optional] 
**RolloverFraction** | **decimal** | Will be passed down to the individual commits. This controls how much of an individual unexpired commit will roll over upon contract transition. Must be between 0 and 1. | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Will be passed down to the individual commits | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Will be passed down to the individual commits | [optional] 
**Specifiers** | [**List&lt;CommitSpecifier&gt;**](CommitSpecifier.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. | [optional] 
**Duration** | [**RelativeDate**](RelativeDate.md) |  | [optional] 
**RecurrenceFrequency** | **string** | The frequency at which the recurring commits will be created. If not provided: - The commits will be created on the usage invoice frequency. If provided: - The period defined in the duration will correspond to this frequency. - Commits will be created aligned with the recurring commit&#39;s starting_at rather than the usage invoice dates. - Daily recurring commits have a limit of one per contract, and are unable to be created with seat-based subscriptions | [optional] 
**Proration** | **string** | Determines whether the first and last commit will be prorated.  If not provided, the default is FIRST_AND_LAST (i.e. prorate both the first and last commits). | [optional] 
**SubscriptionConfig** | [**RecurringCommitSubscriptionConfigTemplate**](RecurringCommitSubscriptionConfigTemplate.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

