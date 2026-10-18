# Org.OpenAPITools.Model.CreatePackagePayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**ContractName** | **string** |  | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**NetPaymentTermsDays** | **decimal** |  | [optional] 
**RateCardId** | **Guid** |  | [optional] 
**RateCardAlias** | **string** | Selects the rate card linked to the specified alias as of the contract&#39;s start date. | [optional] 
**Aliases** | [**List&lt;PackageAlias&gt;**](PackageAlias.md) | Reference this alias when creating a contract. If the same alias is assigned to multiple packages, it will reference the package to which it was most recently assigned. It is not exposed to end customers. | [optional] 
**Duration** | [**RelativeDate**](RelativeDate.md) |  | [optional] 
**Commits** | [**List&lt;CommitTemplateInput&gt;**](CommitTemplateInput.md) |  | [optional] 
**Credits** | [**List&lt;CreditTemplateInput&gt;**](CreditTemplateInput.md) |  | [optional] 
**RecurringCommits** | [**List&lt;RecurringCommitTemplateInput&gt;**](RecurringCommitTemplateInput.md) |  | [optional] 
**RecurringCredits** | [**List&lt;RecurringCreditTemplateInput&gt;**](RecurringCreditTemplateInput.md) |  | [optional] 
**MultiplierOverridePrioritization** | **string** | Defaults to LOWEST_MULTIPLIER, which applies the greatest discount to list prices automatically. EXPLICIT prioritization requires specifying priorities for each multiplier; the one with the lowest priority value will be prioritized first. If tiered overrides are used, prioritization must be explicit. | [optional] 
**Overrides** | [**List&lt;OverrideTemplateInput&gt;**](OverrideTemplateInput.md) |  | [optional] 
**ScheduledCharges** | [**List&lt;ScheduledChargeTemplateInput&gt;**](ScheduledChargeTemplateInput.md) |  | [optional] 
**ScheduledChargesOnUsageInvoices** | **ScheduledChargesOnUsageInvoices** |  | [optional] 
**UsageStatementSchedule** | [**UsageStatementScheduleTemplateInput**](UsageStatementScheduleTemplateInput.md) |  | [optional] 
**BillingProvider** | **ContractsBillingProviderType** |  | [optional] 
**DeliveryMethod** | **BillingProviderDeliveryMethodType** |  | [optional] 
**SpendThresholdConfiguration** | [**SpendThresholdConfiguration**](SpendThresholdConfiguration.md) |  | [optional] 
**PrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfiguration**](PrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**SpendTrackers** | [**List&lt;SpendTrackerInput&gt;**](SpendTrackerInput.md) |  | [optional] 
**Subscriptions** | [**List&lt;SubscriptionTemplateInput&gt;**](SubscriptionTemplateInput.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

