# Org.OpenAPITools.Model.CreateContractPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**StartingAt** | **DateTime** | inclusive contract start time | 
**PackageId** | **Guid** | If provided, provisions a customer on a package instead of creating a traditional contract. When specified, only customer_id, starting_at, package_id, uniqueness_key, transition, and custom_fields are allowed. | [optional] 
**PackageAlias** | **string** | Selects the package linked to the specified alias as of the contract&#39;s start date. Mutually exclusive with package_id. | [optional] 
**PackageCustomizations** | [**PackageCustomizations**](PackageCustomizations.md) |  | [optional] 
**Name** | **string** |  | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetPaymentTermsDays** | **decimal** |  | [optional] 
**RateCardId** | **Guid** |  | [optional] 
**RateCardAlias** | **string** | Selects the rate card linked to the specified alias as of the contract&#39;s start date. | [optional] 
**TotalContractValue** | **decimal** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**EndingBefore** | **DateTime** | exclusive contract end time | [optional] 
**Commits** | [**List&lt;CommitInput&gt;**](CommitInput.md) |  | [optional] 
**Credits** | [**List&lt;CreditInput&gt;**](CreditInput.md) |  | [optional] 
**RecurringCommits** | [**List&lt;RecurringCommitInput&gt;**](RecurringCommitInput.md) |  | [optional] 
**RecurringCredits** | [**List&lt;RecurringCreditInput&gt;**](RecurringCreditInput.md) |  | [optional] 
**MultiplierOverridePrioritization** | **string** | Defaults to LOWEST_MULTIPLIER, which applies the greatest discount to list prices automatically. EXPLICIT prioritization requires specifying priorities for each multiplier; the one with the lowest priority value will be prioritized first. If tiered overrides are used, prioritization must be explicit. | [optional] 
**Overrides** | [**List&lt;OverrideInput&gt;**](OverrideInput.md) |  | [optional] 
**Discounts** | [**List&lt;DiscountInput&gt;**](DiscountInput.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ProfessionalServices** | [**List&lt;ProServiceInput&gt;**](ProServiceInput.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ResellerRoyalties** | [**List&lt;ResellerRoyaltyInput&gt;**](ResellerRoyaltyInput.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ScheduledCharges** | [**List&lt;ScheduledChargeInput&gt;**](ScheduledChargeInput.md) |  | [optional] 
**ScheduledChargesOnUsageInvoices** | **ScheduledChargesOnUsageInvoices** |  | [optional] 
**Transition** | [**ContractTransitionInput**](ContractTransitionInput.md) |  | [optional] 
**UsageFilter** | [**BaseUsageFilter**](BaseUsageFilter.md) |  | [optional] 
**UsageStatementSchedule** | [**UsageStatementScheduleInput**](UsageStatementScheduleInput.md) |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**BillingProviderConfiguration** | [**CustomerBillingProviderConfigurationLookup**](CustomerBillingProviderConfigurationLookup.md) |  | [optional] 
**RevenueSystemConfiguration** | [**CustomerRevenueSystemConfigurationLookup**](CustomerRevenueSystemConfigurationLookup.md) |  | [optional] 
**SpendThresholdConfiguration** | [**SpendThresholdConfiguration**](SpendThresholdConfiguration.md) |  | [optional] 
**PrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfiguration**](PrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**SpendTrackers** | [**List&lt;SpendTrackerInput&gt;**](SpendTrackerInput.md) | Spend trackers to attach to this contract. Aliases must be unique within a contract. | [optional] 
**Subscriptions** | [**List&lt;SubscriptionInput&gt;**](SubscriptionInput.md) | Optional list of [subscriptions](https://docs.metronome.com/manage-product-access/create-subscription/) to add to the contract. | [optional] 
**HierarchyConfiguration** | [**ContractHierarchyConfigurationInput**](ContractHierarchyConfigurationInput.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

