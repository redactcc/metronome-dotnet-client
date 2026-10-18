# Org.OpenAPITools.Model.Contract

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**CustomerId** | **Guid** |  | 
**Initial** | [**ContractWithoutAmendments**](ContractWithoutAmendments.md) |  | 
**Current** | [**ContractWithoutAmendments**](ContractWithoutAmendments.md) |  | 
**Amendments** | [**List&lt;ContractAmendment&gt;**](ContractAmendment.md) |  | 
**ArchivedAt** | **DateTime** | RFC 3339 timestamp indicating when the contract was archived. If not returned, the contract is not archived. | [optional] 
**PackageId** | **Guid** | ID of the package this contract was created from, if applicable. | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**CustomerBillingProviderConfiguration** | [**CustomerBillingProviderConfiguration**](CustomerBillingProviderConfiguration.md) |  | [optional] 
**ScheduledChargesOnUsageInvoices** | **ScheduledChargesOnUsageInvoices** |  | [optional] 
**Subscriptions** | [**List&lt;Subscription&gt;**](Subscription.md) | List of subscriptions on the contract. | [optional] 
**SpendThresholdConfiguration** | [**SpendThresholdConfiguration**](SpendThresholdConfiguration.md) |  | [optional] 
**PrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfiguration**](PrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**SpendTrackers** | [**List&lt;ContractWithoutAmendmentsSpendTrackersInner&gt;**](ContractWithoutAmendmentsSpendTrackersInner.md) | Spend trackers attached to this contract. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

