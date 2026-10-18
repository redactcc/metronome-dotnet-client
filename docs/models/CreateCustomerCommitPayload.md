# Org.OpenAPITools.Model.CreateCustomerCommitPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**Type** | **string** |  | 
**Priority** | **decimal** | If multiple credits or commits are applicable, the one with the lower priority will apply first. | 
**ProductId** | **Guid** | ID of the fixed product associated with the commit. This is required because products are used to invoice the commit amount. | 
**AccessSchedule** | [**ScheduleDurationInput**](ScheduleDurationInput.md) |  | 
**RateType** | **string** |  | [optional] 
**Name** | **string** | displayed on invoices | [optional] 
**Description** | **string** | Used only in UI/API. It is not exposed to end customers. | [optional] 
**InvoiceSchedule** | [**SchedulePointInTimeInput**](SchedulePointInTimeInput.md) |  | [optional] 
**InvoiceContractId** | **Guid** | The contract that this commit will be billed on. This is required for \&quot;POSTPAID\&quot; commits and for \&quot;PREPAID\&quot; commits unless there is no invoice schedule above (i.e., the commit is &#39;free&#39;), or if do_not_invoice is set to true. | [optional] 
**ApplicableProductIds** | **List&lt;Guid&gt;** | Which products the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ApplicableProductTags** | **List&lt;string&gt;** | Which tags the commit applies to. If applicable_product_ids, applicable_product_tags or specifiers are not provided, the commit applies to all products. | [optional] 
**ApplicableContractIds** | **List&lt;string&gt;** | Which contract the commit applies to. If not provided, the commit applies to all contracts. | [optional] 
**Specifiers** | [**List&lt;CommitSpecifierInput&gt;**](CommitSpecifierInput.md) | List of filters that determine what kind of customer usage draws down a commit or credit. A customer&#39;s usage needs to meet the condition of at least one of the specifiers to contribute to a commit&#39;s or credit&#39;s drawdown. This field cannot be used together with &#x60;applicable_product_ids&#x60; or &#x60;applicable_product_tags&#x60;. | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a commit or credit is made with a uniqueness key that was previously used to create a commit or credit, a new record will not be created and the request will fail with a 409 error. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

