# Org.OpenAPITools.Model.EditContractPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose contract is being edited | 
**ContractId** | **Guid** | ID of the contract being edited | 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**AddCommits** | [**List&lt;CommitInputV2&gt;**](CommitInputV2.md) |  | [optional] 
**AddCredits** | [**List&lt;CreditInputV2&gt;**](CreditInputV2.md) |  | [optional] 
**AddRecurringCommits** | [**List&lt;RecurringCommitInputV2&gt;**](RecurringCommitInputV2.md) |  | [optional] 
**AddRecurringCredits** | [**List&lt;RecurringCreditInputV2&gt;**](RecurringCreditInputV2.md) |  | [optional] 
**AddDiscounts** | [**List&lt;DiscountInputV2&gt;**](DiscountInputV2.md) |  | [optional] 
**AddOverrides** | [**List&lt;OverrideInputV2&gt;**](OverrideInputV2.md) |  | [optional] 
**AddScheduledCharges** | [**List&lt;ScheduledChargeInputV2&gt;**](ScheduledChargeInputV2.md) |  | [optional] 
**AddProfessionalServices** | [**List&lt;ProServiceInput&gt;**](ProServiceInput.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**AddResellerRoyalties** | [**List&lt;ResellerRoyaltyOrUpdateInput&gt;**](ResellerRoyaltyOrUpdateInput.md) |  | [optional] 
**AddSubscriptions** | [**List&lt;SubscriptionInputV2&gt;**](SubscriptionInputV2.md) | Optional list of [subscriptions](https://docs.metronome.com/manage-product-access/create-subscription/) to add to the contract. | [optional] 
**AddSpendThresholdConfiguration** | [**SpendThresholdConfigurationV2**](SpendThresholdConfigurationV2.md) |  | [optional] 
**AddPrepaidBalanceThresholdConfiguration** | [**PrepaidBalanceThresholdConfigurationV2**](PrepaidBalanceThresholdConfigurationV2.md) |  | [optional] 
**AddBillingProviderConfigurationUpdate** | [**BillingProviderConfigurationUpdate**](BillingProviderConfigurationUpdate.md) |  | [optional] 
**AddRevenueSystemConfigurationUpdate** | [**RevenueSystemConfigurationUpdate**](RevenueSystemConfigurationUpdate.md) |  | [optional] 
**AddSpendTrackers** | [**List&lt;SpendTrackerInput&gt;**](SpendTrackerInput.md) | Spend trackers to add to this contract. Aliases must be unique within a contract. | [optional] 
**UpdateContractName** | **string** | Value to update the contract name to. If not provided, the contract name will remain unchanged. | [optional] 
**UpdateScheduledCharges** | [**List&lt;UpdateScheduledChargeInput&gt;**](UpdateScheduledChargeInput.md) |  | [optional] 
**UpdateCommits** | [**List&lt;UpdateCommitInput&gt;**](UpdateCommitInput.md) |  | [optional] 
**UpdateCredits** | [**List&lt;UpdateCreditInput&gt;**](UpdateCreditInput.md) |  | [optional] 
**UpdateRecurringCommits** | [**List&lt;UpdateRecurringCommitInput&gt;**](UpdateRecurringCommitInput.md) | Edits to these recurring commits will only affect commits whose access schedules has not started. Expired commits, and commits with an active access schedule will remain unchanged. | [optional] 
**UpdateRecurringCredits** | [**List&lt;UpdateRecurringCreditInput&gt;**](UpdateRecurringCreditInput.md) | Edits to these recurring credits will only affect credits whose access schedules has not started. Expired credits, and credits with an active access schedule will remain unchanged. | [optional] 
**UpdateSubscriptions** | [**List&lt;UpdateSubscriptionInput&gt;**](UpdateSubscriptionInput.md) | Optional list of subscriptions to update. | [optional] 
**UpdateSpendThresholdConfiguration** | [**UpdateSpendThresholdConfiguration**](UpdateSpendThresholdConfiguration.md) |  | [optional] 
**UpdatePrepaidBalanceThresholdConfiguration** | [**UpdatePrepaidBalanceThresholdConfiguration**](UpdatePrepaidBalanceThresholdConfiguration.md) |  | [optional] 
**UpdateContractEndDate** | **DateTime** | RFC 3339 timestamp indicating when the contract will end (exclusive). | [optional] 
**UpdateNetPaymentTermsDays** | **decimal** | Number of days after issuance of invoice after which the invoice is due (e.g. Net 30). | [optional] 
**AllowContractEndingBeforeFinalizedInvoice** | **bool** | If true, allows setting the contract end date earlier than the end_timestamp of existing finalized invoices. Finalized invoices will be unchanged; if you want to incorporate the new end date, you can void and regenerate finalized usage invoices. Defaults to true. | [optional] 
**ArchiveCommits** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) | IDs of commits to archive | [optional] 
**ArchiveCredits** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) | IDs of credits to archive | [optional] 
**ArchiveScheduledCharges** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) | IDs of scheduled charges to archive | [optional] 
**ArchiveSpendTrackers** | **List&lt;string&gt;** | Aliases of spend trackers to archive. | [optional] 
**RemoveOverrides** | [**List&lt;VoidInvoiceV1200ResponseData&gt;**](VoidInvoiceV1200ResponseData.md) | IDs of overrides to remove | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

