# Org.OpenAPITools.Model.CreateNotificationConfigPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | The name for this offset notification configuration.  | 
**Policy** | [**LifecycleEventOffsetPolicy**](LifecycleEventOffsetPolicy.md) |  | 
**UniquenessKey** | **string** | Prevents the creation of duplicates. If a request to create a record is made with a previously used uniqueness key, a new record will not be created and the request will fail with a 409 error. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

