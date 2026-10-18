# Org.OpenAPITools.Model.Commit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Type** | **string** |  | 
**Product** | [**SubscriptionRateProduct**](SubscriptionRateProduct.md) |  | 
**CreatedAt** | **DateTime** | Timestamp of when the commit was created. - Recurring commits: latter of commit service period date and parent commit start date - Rollover commits: when the new contract started  | 
**Contract** | [**VoidInvoiceV1200ResponseData**](VoidInvoiceV1200ResponseData.md) |  | [optional] 
**RateType** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**Priority** | **decimal** | If multiple credits or commits are applicable, the one with the lower priority will apply first. | [optional] 
**CostBasis** | **decimal** | The ratio of the amount paid for the commit to the amount of credit granted. | [optional] 
**AccessSchedule** | [**ScheduleDuration**](ScheduleDuration.md) |  | [optional] 
**InvoiceSchedule** | [**SchedulePointInTime**](SchedulePointInTime.md) |  | [optional] 
**InvoiceContract** | [**CommitInvoiceContract**](CommitInvoiceContract.md) |  | [optional] 
**RecurringCommitId** | **Guid** | The ID of the recurring commit that this commit was generated from, if applicable. | [optional] 
**SubscriptionConfig** | [**CommitSubscriptionConfig**](CommitSubscriptionConfig.md) |  | [optional] 
**RolledOverFrom** | [**CommitRolledOverFrom**](CommitRolledOverFrom.md) |  | [optional] 
**Description** | **string** |  | [optional] 
**RolloverFraction** | **decimal** |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** |  | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** |  | [optional] 
**Specifiers** | [**List&lt;CommitSpecifier&gt;**](CommitSpecifier.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. | [optional] 
**ApplicableContractIds** | **List&lt;Guid&gt;** |  | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**Amount** | **decimal** | (DEPRECATED) Use access_schedule + invoice_schedule instead. | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**Ledger** | [**List&lt;CommitLedger&gt;**](CommitLedger.md) | A list of ordered events that impact the balance of a commit. For example, an invoice deduction or a rollover. | [optional] 
**Balance** | **decimal** | The current balance of the credit or commit. This balance reflects the amount of credit or commit that the customer has access to use at this moment - thus, expired and upcoming credit or commit segments contribute 0 to the balance. The balance will match the sum of all ledger entries with the exception of the case where the sum of negative manual ledger entries exceeds the positive amount remaining on the credit or commit - in that case, the balance will be 0. All manual ledger entries associated with active credit or commit segments are included in the balance, including future-dated manual ledger entries. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a commit or credit is made with a uniqueness key that was previously used to create a commit or credit, a new record will not be created and the request will fail with a 409 error. | [optional] 
**ArchivedAt** | **DateTime** | RFC 3339 timestamp indicating when the commit was archived. If not provided, the commit is not archived. | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 
**SpendTrackerAttributes** | [**SpendTrackerAttributes**](SpendTrackerAttributes.md) |  | [optional] 
**CreatedBy** | **string** | The actor who created this commit. Omitted for system-generated commits such as recurring commits, rollover commits, and threshold commits. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

