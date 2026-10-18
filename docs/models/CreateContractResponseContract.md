# Org.OpenAPITools.Model.CreateContractResponseContract
The created contract.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**CustomerId** | **Guid** |  | 
**CreatedAt** | **DateTime** |  | 
**CreatedBy** | **string** |  | 
**StartingAt** | **DateTime** |  | 
**UsageStatementSchedule** | [**UsageStatementSchedule**](UsageStatementSchedule.md) |  | 
**UsageFilter** | [**List&lt;CreateContractResponseContractUsageFilterInner&gt;**](CreateContractResponseContractUsageFilterInner.md) |  | 
**Commits** | [**List&lt;Commit&gt;**](Commit.md) |  | 
**Overrides** | [**List&lt;Override&gt;**](Override.md) |  | 
**ScheduledCharges** | [**List&lt;ScheduledCharge&gt;**](ScheduledCharge.md) |  | 
**Transitions** | [**List&lt;ContractTransition&gt;**](ContractTransition.md) |  | 
**Name** | **string** |  | [optional] 
**PackageId** | **Guid** | ID of the package this contract was created from, if applicable. | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**RateCardId** | **Guid** |  | [optional] 
**EndingBefore** | **DateTime** |  | [optional] 
**NetPaymentTermsDays** | **decimal** |  | [optional] 
**MultiplierOverridePrioritization** | **string** | Defaults to LOWEST_MULTIPLIER, which applies the greatest discount to list prices automatically. EXPLICIT prioritization requires specifying priorities for each multiplier; the one with the lowest priority value will be prioritized first. | [optional] 
**ScheduledChargesOnUsageInvoices** | **ScheduledChargesOnUsageInvoices** |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**Credits** | [**List&lt;Credit&gt;**](Credit.md) |  | [optional] 
**HasMore** | [**HasMore**](HasMore.md) |  | [optional] 
**RecurringCommits** | [**List&lt;RecurringCommit&gt;**](RecurringCommit.md) |  | [optional] 
**RecurringCredits** | [**List&lt;RecurringCredit&gt;**](RecurringCredit.md) |  | [optional] 
**Subscriptions** | [**List&lt;Subscription&gt;**](Subscription.md) | List of subscriptions on the contract. | [optional] 
**CustomerBillingProviderConfiguration** | [**CustomerBillingProviderConfiguration**](CustomerBillingProviderConfiguration.md) |  | [optional] 
**SpendThresholdConfiguration** | [**SpendThresholdConfiguration**](SpendThresholdConfiguration.md) |  | [optional] 
**PrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfiguration**](PrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**HierarchyConfiguration** | [**HierarchyConfiguration**](HierarchyConfiguration.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

