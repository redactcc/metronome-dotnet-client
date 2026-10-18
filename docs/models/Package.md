# Org.OpenAPITools.Model.Package

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Commits** | [**List&lt;CommitTemplate&gt;**](CommitTemplate.md) |  | 
**Overrides** | [**List&lt;OverrideTemplate&gt;**](OverrideTemplate.md) |  | 
**ScheduledCharges** | [**List&lt;ScheduledChargeTemplate&gt;**](ScheduledChargeTemplate.md) |  | 
**CreatedAt** | **DateTime** |  | 
**CreatedBy** | **string** |  | 
**UsageStatementSchedule** | [**UsageStatementScheduleTemplate**](UsageStatementScheduleTemplate.md) |  | 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**Name** | **string** |  | [optional] 
**RateCardId** | **Guid** |  | [optional] 
**Aliases** | [**List&lt;PackageAlias&gt;**](PackageAlias.md) |  | [optional] 
**Duration** | [**RelativeDate**](RelativeDate.md) |  | [optional] 
**Credits** | [**List&lt;CreditTemplate&gt;**](CreditTemplate.md) |  | [optional] 
**ScheduledChargesOnUsageInvoices** | **ScheduledChargesOnUsageInvoices** |  | [optional] 
**NetPaymentTermsDays** | **decimal** |  | [optional] 
**MultiplierOverridePrioritization** | **string** | Defaults to LOWEST_MULTIPLIER, which applies the greatest discount to list prices automatically. EXPLICIT prioritization requires specifying priorities for each multiplier; the one with the lowest priority value will be prioritized first. | [optional] 
**BillingProvider** | **BillingProviderType** |  | [optional] 
**DeliveryMethod** | **BillingProviderDeliveryMethodType** |  | [optional] 
**RecurringCommits** | [**List&lt;RecurringCommitTemplate&gt;**](RecurringCommitTemplate.md) |  | [optional] 
**RecurringCredits** | [**List&lt;RecurringCreditTemplate&gt;**](RecurringCreditTemplate.md) |  | [optional] 
**SpendThresholdConfiguration** | [**SpendThresholdConfiguration**](SpendThresholdConfiguration.md) |  | [optional] 
**PrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfiguration**](PrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**SpendTrackers** | [**List&lt;SpendTrackerTemplate&gt;**](SpendTrackerTemplate.md) |  | [optional] 
**Subscriptions** | [**List&lt;SubscriptionTemplate&gt;**](SubscriptionTemplate.md) |  | [optional] 
**ContractName** | **string** | The name to use for contracts created from this package. | [optional] 
**ArchivedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

