# Org.OpenAPITools.Model.PackageCustomizations
Adjustments applied on top of the package's baseline configuration when provisioning the contract. Availability is gated.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ModifySubscriptions** | [**List&lt;PackageSubscriptionCustomization&gt;**](PackageSubscriptionCustomization.md) | Per-subscription overrides for the subscriptions defined on the package template. Each entry targets one template subscription and sets its starting quantity or seats. | [optional] 
**AddOverrides** | [**List&lt;OverrideInput&gt;**](OverrideInput.md) | Rate overrides layered onto the contract on top of the package&#39;s baseline configuration. Same shape as create_contract&#39;s overrides. | [optional] 
**AddCommits** | [**List&lt;CommitInput&gt;**](CommitInput.md) | Commits added to the contract on top of the package&#39;s baseline configuration. Same shape as create_contract&#39;s commits. | [optional] 
**AddCredits** | [**List&lt;CreditInput&gt;**](CreditInput.md) | Credits added to the contract on top of the package&#39;s baseline configuration. Same shape as create_contract&#39;s credits. | [optional] 
**AddRecurringCommits** | [**List&lt;RecurringCommitInput&gt;**](RecurringCommitInput.md) | Recurring commits added to the contract on top of the package&#39;s baseline configuration. Same shape as create_contract&#39;s recurring_commits. | [optional] 
**AddRecurringCredits** | [**List&lt;RecurringCreditInput&gt;**](RecurringCreditInput.md) | Recurring credits added to the contract on top of the package&#39;s baseline configuration. Same shape as create_contract&#39;s recurring_credits. | [optional] 
**AddScheduledCharges** | [**List&lt;ScheduledChargeInput&gt;**](ScheduledChargeInput.md) | Scheduled charges added to the contract on top of the package&#39;s baseline configuration. Same shape as create_contract&#39;s scheduled_charges. | [optional] 
**AddSpendTrackers** | [**List&lt;SpendTrackerInput&gt;**](SpendTrackerInput.md) | Spend trackers added to the contract on top of the package&#39;s baseline configuration. Same shape as create_contract&#39;s spend_trackers; aliases must be unique within a contract. | [optional] 
**AddSubscriptions** | [**List&lt;SubscriptionInput&gt;**](SubscriptionInput.md) | Optional list of [subscriptions](https://docs.metronome.com/manage-product-access/create-subscription/) to add to the contract. | [optional] 
**SetSpendThresholdConfiguration** | [**SpendThresholdConfiguration**](SpendThresholdConfiguration.md) |  | [optional] 
**SetPrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfiguration**](PrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**ModifyUsageStatementSchedule** | [**PackageCustomizationsModifyUsageStatementSchedule**](PackageCustomizationsModifyUsageStatementSchedule.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

