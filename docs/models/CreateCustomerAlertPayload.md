# Org.OpenAPITools.Model.CreateCustomerAlertPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AlertType** | **string** | Type of the threshold notification | 
**Name** | **string** | Name of the threshold notification | 
**Threshold** | **decimal** | Threshold value of the notification policy.  Depending upon the notification type, this number may represent a financial amount, the days remaining, or a percentage reached. | 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 
**CreditTypeId** | **Guid** | ID of the credit&#39;s currency, defaults to USD. If the specific notification type requires a pricing unit/currency, find the ID in the [Metronome app](https://app.metronome.com/offering/pricing-units). | [optional] 
**CustomerId** | **Guid** | If provided, will create this threshold notification for this specific customer. To create a notification for all customers, do not specify a &#x60;customer_id&#x60;. | [optional] 
**BillableMetricId** | **Guid** | For threshold notifications of type &#x60;usage_threshold_reached&#x60;, specifies which billable metric to track the usage for. | [optional] 
**CreditGrantTypeFilters** | **List&lt;string&gt;** | An array of strings, representing a way to filter the credit grant this threshold notification applies to, by looking at the credit_grant_type field on the credit grant. This field is only defined for CreditPercentage and CreditBalance notifications | [optional] 
**EvaluateOnCreate** | **bool** | If true, the threshold notification will evaluate immediately on customers that already meet the notification threshold. If false, it will only evaluate on future customers that trigger the threshold. Defaults to true. | [optional] 
**CustomFieldFilters** | [**List&lt;CustomFieldFilterType&gt;**](CustomFieldFilterType.md) | A list of custom field filters for threshold notification types that support advanced filtering. Only present for contract invoices. | [optional] 
**InvoiceTypesFilter** | **List&lt;string&gt;** | Only supported for invoice_total_reached threshold notifications. A list of invoice types to evaluate. | [optional] 
**GroupValues** | [**List&lt;GroupValueFilterType&gt;**](GroupValueFilterType.md) | Only present for &#x60;spend_threshold_reached&#x60; notifications. Scope notification to a specific group key on individual line items. | [optional] 
**SeatFilter** | [**CreateCustomerAlertPayloadSeatFilter**](CreateCustomerAlertPayloadSeatFilter.md) |  | [optional] 
**AccessType** | **string** | Filters the notification to commits/credits with this access type. Only supported for &#x60;low_remaining_commit_balance_reached&#x60;, &#x60;low_remaining_commit_percentage_reached&#x60;, &#x60;low_remaining_contract_credit_and_commit_balance_reached&#x60;, &#x60;low_remaining_contract_credit_and_commit_percentage_reached&#x60;, &#x60;low_remaining_contract_credit_balance_reached&#x60;, &#x60;low_remaining_contract_credit_percentage_reached&#x60;, and &#x60;low_remaining_seat_balance_reached&#x60; notifications. Credit type cannot be specified if using QUANTITY access type. | [optional] 
**AlertSpecifiers** | [**List&lt;AlertSpecifier&gt;**](AlertSpecifier.md) | Can be used only with &#x60;low_remaining_contract_credit_and_commit_balance_reached&#x60; and &#x60;low_remaining_contract_credit_and_commit_percentage_reached&#x60; notifications. Defines the commits and credits used to calculate the remaining balance or percentage. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

