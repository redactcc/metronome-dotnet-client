# Org.OpenAPITools.Model.ContractV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**CustomerId** | **Guid** |  | 
**StartingAt** | **DateTime** |  | 
**Commits** | [**List&lt;CommitV2&gt;**](CommitV2.md) |  | 
**Overrides** | [**List&lt;OverrideV2&gt;**](OverrideV2.md) |  | 
**ScheduledCharges** | [**List&lt;ScheduledCharge&gt;**](ScheduledCharge.md) |  | 
**Transitions** | [**List&lt;ContractTransition&gt;**](ContractTransition.md) |  | 
**CreatedAt** | **DateTime** |  | 
**CreatedBy** | **string** |  | 
**UsageFilter** | [**List&lt;UsageFilterV2&gt;**](UsageFilterV2.md) |  | 
**UsageStatementSchedule** | [**UsageStatementSchedule**](UsageStatementSchedule.md) |  | 
**PackageId** | **Guid** | (BETA) ID of the package this contract was created from, if applicable. | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**Name** | **string** |  | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**RateCardId** | **Guid** |  | [optional] 
**Credits** | [**List&lt;CreditV2&gt;**](CreditV2.md) |  | [optional] 
**HasMore** | [**HasMore**](HasMore.md) |  | [optional] 
**Discounts** | [**List&lt;Discount&gt;**](Discount.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ProfessionalServices** | [**List&lt;ProService&gt;**](ProService.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ScheduledChargesOnUsageInvoices** | **ScheduledChargesOnUsageInvoices** |  | [optional] 
**ResellerRoyalties** | [**List&lt;ContractV2ResellerRoyaltiesInner&gt;**](ContractV2ResellerRoyaltiesInner.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetPaymentTermsDays** | **decimal** |  | [optional] 
**EndingBefore** | **DateTime** |  | [optional] 
**ArchivedAt** | **DateTime** |  | [optional] 
**TotalContractValue** | **decimal** |  | [optional] 
**MultiplierOverridePrioritization** | **string** | Defaults to LOWEST_MULTIPLIER, which applies the greatest discount to list prices automatically. EXPLICIT prioritization requires specifying priorities for each multiplier; the one with the lowest priority value will be prioritized first. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**CustomerBillingProviderConfiguration** | [**CustomerBillingProviderConfiguration**](CustomerBillingProviderConfiguration.md) |  | [optional] 
**BillingProviderConfigurationSchedule** | [**List&lt;ContractV2BillingProviderConfigurationScheduleInner&gt;**](ContractV2BillingProviderConfigurationScheduleInner.md) | The schedule of billing provider configuration changes on the contract, ordered by effective_at ascending. | [optional] 
**RevenueSystemConfigurationSchedule** | [**List&lt;ContractV2RevenueSystemConfigurationScheduleInner&gt;**](ContractV2RevenueSystemConfigurationScheduleInner.md) | The schedule of revenue system configuration changes on the contract, ordered by effective_at ascending. | [optional] 
**RecurringCommits** | [**List&lt;RecurringCommitV2&gt;**](RecurringCommitV2.md) |  | [optional] 
**RecurringCredits** | [**List&lt;RecurringCreditV2&gt;**](RecurringCreditV2.md) |  | [optional] 
**SpendThresholdConfiguration** | [**SpendThresholdConfigurationV2**](SpendThresholdConfigurationV2.md) |  | [optional] 
**PrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfigurationV2**](PrepaidBalanceThresholdConfigurationV2.md) |  | [optional] 
**SpendTrackers** | [**List&lt;SpendTracker&gt;**](SpendTracker.md) | Spend trackers attached to this contract. | [optional] 
**Subscriptions** | [**List&lt;SubscriptionV2&gt;**](SubscriptionV2.md) | List of subscriptions on the contract. | [optional] 
**HierarchyConfiguration** | [**HierarchyConfigurationV2**](HierarchyConfigurationV2.md) |  | [optional] 
**Priority** | **decimal** | Priority of the contract. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

