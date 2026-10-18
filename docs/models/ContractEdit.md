# Org.OpenAPITools.Model.ContractEdit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Timestamp** | **DateTime** |  | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**AddOverrides** | [**List&lt;OverrideV2&gt;**](OverrideV2.md) |  | [optional] 
**AddProServices** | [**List&lt;ProService&gt;**](ProService.md) |  | [optional] 
**AddResellerRoyalties** | [**List&lt;ResellerRoyaltyOrUpdateV2&gt;**](ResellerRoyaltyOrUpdateV2.md) |  | [optional] 
**AddDiscounts** | [**List&lt;Discount&gt;**](Discount.md) |  | [optional] 
**AddScheduledCharges** | [**List&lt;ScheduledChargeAdd&gt;**](ScheduledChargeAdd.md) |  | [optional] 
**AddCommits** | [**List&lt;CommitAdd&gt;**](CommitAdd.md) |  | [optional] 
**AddCredits** | [**List&lt;CreditAdd&gt;**](CreditAdd.md) |  | [optional] 
**AddRecurringCommits** | [**List&lt;RecurringCommitV2&gt;**](RecurringCommitV2.md) |  | [optional] 
**AddRecurringCredits** | [**List&lt;RecurringCreditV2&gt;**](RecurringCreditV2.md) |  | [optional] 
**AddUsageFilters** | [**List&lt;UsageFilterV2&gt;**](UsageFilterV2.md) |  | [optional] 
**AddSubscriptions** | [**List&lt;SubscriptionV2&gt;**](SubscriptionV2.md) | List of subscriptions on the contract. | [optional] 
**AddPrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfigurationV2**](PrepaidBalanceThresholdConfigurationV2.md) |  | [optional] 
**AddSpendThresholdConfiguration** | [**SpendThresholdConfigurationV2**](SpendThresholdConfigurationV2.md) |  | [optional] 
**UpdateContractName** | **string** | Value to update the contract name to. If not provided, the contract name will remain unchanged. | [optional] 
**UpdateDiscounts** | [**List&lt;DiscountUpdate&gt;**](DiscountUpdate.md) |  | [optional] 
**UpdateScheduledCharges** | [**List&lt;ScheduledChargeUpdate&gt;**](ScheduledChargeUpdate.md) |  | [optional] 
**UpdateCommits** | [**List&lt;CommitUpdate&gt;**](CommitUpdate.md) |  | [optional] 
**UpdateCredits** | [**List&lt;CreditUpdate&gt;**](CreditUpdate.md) |  | [optional] 
**UpdateRecurringCommits** | [**List&lt;RecurringCommitUpdate&gt;**](RecurringCommitUpdate.md) |  | [optional] 
**UpdateRecurringCredits** | [**List&lt;RecurringCreditUpdate&gt;**](RecurringCreditUpdate.md) |  | [optional] 
**UpdateContractEndDate** | **DateTime** |  | [optional] 
**UpdateRefundInvoices** | [**List&lt;RefundInvoiceUpdate&gt;**](RefundInvoiceUpdate.md) |  | [optional] 
**UpdateSubscriptions** | [**List&lt;SubscriptionsUpdate&gt;**](SubscriptionsUpdate.md) | Optional list of subscriptions to update. | [optional] 
**UpdatePrepaidBalanceThresholdConfiguration** | [**UpdatePrepaidBalanceThresholdConfiguration**](UpdatePrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**UpdateSpendThresholdConfiguration** | [**UpdateSpendThresholdConfiguration**](UpdateSpendThresholdConfiguration.md) |  | [optional] 
**ArchiveCommits** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) |  | [optional] 
**ArchiveCredits** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) |  | [optional] 
**ArchiveScheduledCharges** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) |  | [optional] 
**RemoveOverrides** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

