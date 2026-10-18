# Org.OpenAPITools.Model.Alert

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | the Metronome ID of the threshold notification | 
**Name** | **string** | Name of the threshold notification | 
**Type** | **string** | Type of the threshold notification | 
**Status** | **string** | Status of the threshold notification | 
**Threshold** | **decimal** | Threshold value of the notification policy | 
**UpdatedAt** | **DateTime** | Timestamp for when the threshold notification&#39;s customer status was last updated | 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**CreditType** | [**CreditType**](CreditType.md) |  | [optional] 
**CreditGrantTypeFilters** | **List&lt;string&gt;** | An array of strings, representing a way to filter the credit grant this threshold notification applies to, by looking at the credit_grant_type field on the credit grant. This field is only defined for CreditPercentage and CreditBalance notifications | [optional] 
**CustomFieldFilters** | [**List&lt;CustomFieldFilterType&gt;**](CustomFieldFilterType.md) | A list of custom field filters for notification types that support advanced filtering | [optional] 
**GroupKeyFilter** | [**GroupKeyFilterType**](GroupKeyFilterType.md) |  | [optional] 
**InvoiceTypesFilter** | **List&lt;string&gt;** | Only supported for invoice_total_reached threshold notifications. A list of invoice types to evaluate. | [optional] 
**GroupValues** | [**List&lt;GroupValueFilterType&gt;**](GroupValueFilterType.md) | Only present for &#x60;spend_threshold_reached&#x60; notifications. Scope notification to a specific group key on individual line items. | [optional] 
**SeatFilter** | [**AlertSeatFilter**](AlertSeatFilter.md) |  | [optional] 
**AccessType** | **string** | Indicates the commit access type this notification is scoped to. Defaults to &#x60;SPEND&#x60; if not otherwise specified. Only present for &#x60;low_remaining_commit_balance_reached&#x60;, &#x60;low_remaining_commit_percentage_reached&#x60;, &#x60;low_remaining_contract_credit_and_commit_balance_reached&#x60;, &#x60;low_remaining_contract_credit_and_commit_percentage_reached&#x60;, &#x60;low_remaining_contract_credit_balance_reached&#x60;, &#x60;low_remaining_contract_credit_percentage_reached&#x60;, and &#x60;low_remaining_seat_balance_reached&#x60; notifications. | [optional] 
**AlertSpecifiers** | [**List&lt;AlertSpecifier&gt;**](AlertSpecifier.md) | Present for &#x60;low_remaining_contract_credit_and_commit_balance_reached&#x60; and &#x60;low_remaining_contract_credit_and_commit_percentage_reached&#x60; notifications. The filters that define the commits and credits used to calculate the remaining balance or percentage. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

