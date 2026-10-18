# Org.OpenAPITools.Model.WebhookDeliveryDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | ID of the triggered notification. | 
**WebhookId** | **Guid** | ID of the webhook destination. | 
**NotificationType** | **string** |  | 
**NotificationPayload** | **string** | The exact payload sent to the webhook destination. | 
**Attempts** | [**List&lt;WebhookDeliveryAttempt&gt;**](WebhookDeliveryAttempt.md) | Delivery attempts ordered from oldest to newest. | 
**CustomerId** | **Guid** |  | 
**NotificationId** | **string** | ID of the notification configuration, when applicable. | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

