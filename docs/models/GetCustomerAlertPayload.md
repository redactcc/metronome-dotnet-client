# Org.OpenAPITools.Model.GetCustomerAlertPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | The Metronome ID of the customer | 
**AlertId** | **Guid** | The Metronome ID of the threshold notification | 
**PlansOrContracts** | **string** | When parallel threshold notifications are enabled during migration, this flag denotes whether to fetch notifications for plans or contracts. | [optional] 
**GroupValues** | [**List&lt;GroupKeyFilterType&gt;**](GroupKeyFilterType.md) | Only present for &#x60;spend_threshold_reached&#x60; notifications. Retrieve the notification for a specific group key-value pair. | [optional] 
**SeatFilter** | [**GetCustomerAlertPayloadSeatFilter**](GetCustomerAlertPayloadSeatFilter.md) |  | [optional] 
**AlertSpecifiers** | [**List&lt;AlertSpecifierFilter&gt;**](AlertSpecifierFilter.md) | Can be used only with &#x60;low_remaining_contract_credit_and_commit_balance_reached&#x60; and &#x60;low_remaining_contract_credit_and_commit_percentage_reached&#x60; notifications. Used to filter the alert by the custom field key-value pair. | [optional] 
**CustomFieldFilters** | [**List&lt;CustomFieldFilterType&gt;**](CustomFieldFilterType.md) | Used to filter the alert by the custom field key-value pair. | [optional] 
**WebhookNotificationId** | **string** | Indicates that this API request was triggered by a webhook notification with the provided ID. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

