# Org.OpenAPITools.Model.ContractWithoutAmendments

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StartingAt** | **DateTime** |  | 
**Commits** | [**List&lt;Commit&gt;**](Commit.md) |  | 
**Overrides** | [**List&lt;Override&gt;**](Override.md) |  | 
**ScheduledCharges** | [**List&lt;ScheduledCharge&gt;**](ScheduledCharge.md) |  | 
**Transitions** | [**List&lt;ContractTransition&gt;**](ContractTransition.md) |  | 
**CreatedAt** | **DateTime** |  | 
**CreatedBy** | **string** |  | 
**UsageStatementSchedule** | [**UsageStatementSchedule**](UsageStatementSchedule.md) |  | 
**Name** | **string** |  | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**RateCardId** | **Guid** |  | [optional] 
**Credits** | [**List&lt;Credit&gt;**](Credit.md) |  | [optional] 
**RecurringCommits** | [**List&lt;RecurringCommit&gt;**](RecurringCommit.md) |  | [optional] 
**RecurringCredits** | [**List&lt;RecurringCredit&gt;**](RecurringCredit.md) |  | [optional] 
**Discounts** | [**List&lt;Discount&gt;**](Discount.md) | This field&#39;s availability is dependent on your client&#39;s | [optional] 
**ProfessionalServices** | [**List&lt;ProService&gt;**](ProService.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ScheduledChargesOnUsageInvoices** | **ScheduledChargesOnUsageInvoices** |  | [optional] 
**ResellerRoyalties** | [**List&lt;ResellerRoyalty&gt;**](ResellerRoyalty.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetPaymentTermsDays** | **decimal** |  | [optional] 
**EndingBefore** | **DateTime** |  | [optional] 
**TotalContractValue** | **decimal** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**UsageFilter** | [**UsageFilter**](UsageFilter.md) |  | [optional] 
**SpendThresholdConfiguration** | [**SpendThresholdConfiguration**](SpendThresholdConfiguration.md) |  | [optional] 
**PrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfiguration**](PrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**SpendTrackers** | [**List&lt;ContractWithoutAmendmentsSpendTrackersInner&gt;**](ContractWithoutAmendmentsSpendTrackersInner.md) | Spend trackers attached to this contract. | [optional] 
**HierarchyConfiguration** | [**HierarchyConfiguration**](HierarchyConfiguration.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

