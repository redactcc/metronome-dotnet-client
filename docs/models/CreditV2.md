# Org.OpenAPITools.Model.CreditV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**Type** | **string** |  | 
**Product** | [**SubscriptionRateProduct**](SubscriptionRateProduct.md) |  | 
**Contract** | [**VoidInvoiceV1200ResponseData**](VoidInvoiceV1200ResponseData.md) |  | [optional] 
**Name** | **string** |  | [optional] 
**Priority** | **decimal** | If multiple credits or commits are applicable, the one with the lower priority will apply first. | [optional] 
**AccessSchedule** | [**ScheduleDuration**](ScheduleDuration.md) |  | [optional] 
**Description** | **string** |  | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** |  | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** |  | [optional] 
**Specifiers** | [**List&lt;CommitSpecifier&gt;**](CommitSpecifier.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. | [optional] 
**ApplicableContractIds** | **List&lt;Guid&gt;** |  | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**Ledger** | [**List&lt;CreditLedgerV2&gt;**](CreditLedgerV2.md) | A list of ordered events that impact the balance of a credit. For example, an invoice deduction or an expiration. | [optional] 
**Balance** | **decimal** | The current balance of the credit or commit. This balance reflects the amount of credit or commit that the customer has access to use at this moment - thus, expired and upcoming credit or commit segments contribute 0 to the balance. The balance will match the sum of all ledger entries with the exception of the case where the sum of negative manual ledger entries exceeds the positive amount remaining on the credit or commit - in that case, the balance will be 0. All manual ledger entries associated with active credit or commit segments are included in the balance, including future-dated manual ledger entries. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**ArchivedAt** | **DateTime** |  | [optional] 
**HierarchyConfiguration** | [**CommitHierarchyConfiguration**](CommitHierarchyConfiguration.md) |  | [optional] 
**RolledOverFrom** | [**CreditRolledOverFrom**](CreditRolledOverFrom.md) |  | [optional] 
**CreatedAt** | **DateTime** | Timestamp of when the credit was created. - Recurring credits: latter of credit service period date and parent credit start date  | [optional] 
**CreatedBy** | **string** | The actor who created this credit. Omitted for system-generated credits such as recurring credits. | [optional] 
**RecurringCreditId** | **Guid** | The ID of the recurring credit that created this credit | [optional] 
**SubscriptionConfig** | [**RecurringCommitSubscriptionConfig**](RecurringCommitSubscriptionConfig.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

