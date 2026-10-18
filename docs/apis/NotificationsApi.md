# Org.OpenAPITools.Api.NotificationsApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveNotificationConfigV2**](NotificationsApi.md#archivenotificationconfigv2) | **POST** /v2/notifications/archive | Archive an offset lifecycle event notification configuration |
| [**CreateNotificationConfigV2**](NotificationsApi.md#createnotificationconfigv2) | **POST** /v2/notifications/create | Create an offset lifecycle event notification configuration |
| [**EditNotificationConfigV2**](NotificationsApi.md#editnotificationconfigv2) | **POST** /v2/notifications/edit | Edit an offset or system notification |
| [**GetNotificationConfigV2**](NotificationsApi.md#getnotificationconfigv2) | **POST** /v2/notifications/get | Get an offset lifecycle event notification configuration |
| [**ListOffsetNotificationConfigsV2**](NotificationsApi.md#listoffsetnotificationconfigsv2) | **POST** /v2/notifications/offset/list | List offset lifecycle event notification configurations |
| [**ListSystemNotificationConfigsV2**](NotificationsApi.md#listsystemnotificationconfigsv2) | **POST** /v2/notifications/system/list | List system notification types |

<a id="archivenotificationconfigv2"></a>
# **ArchiveNotificationConfigV2**
> CreateNotificationConfigV2200Response ArchiveNotificationConfigV2 (ArchiveNotificationConfigPayload archiveNotificationConfigPayload = null)

Archive an offset lifecycle event notification configuration

Archive an offset lifecycle event notification configuration. Archived notifications are not processed. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **archiveNotificationConfigPayload** | [**ArchiveNotificationConfigPayload**](ArchiveNotificationConfigPayload.md) | Offset notification configuration ID to archive | [optional]  |

### Return type

[**CreateNotificationConfigV2200Response**](CreateNotificationConfigV2200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Error |  -  |
| **404** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createnotificationconfigv2"></a>
# **CreateNotificationConfigV2**
> CreateNotificationConfigV2200Response CreateNotificationConfigV2 (CreateNotificationConfigPayload createNotificationConfigPayload = null)

Create an offset lifecycle event notification configuration

Create an offset lifecycle event notification configuration. The lifecycle event type is inferred from the policy.type field. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createNotificationConfigPayload** | [**CreateNotificationConfigPayload**](CreateNotificationConfigPayload.md) | Notification configuration details | [optional]  |

### Return type

[**CreateNotificationConfigV2200Response**](CreateNotificationConfigV2200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="editnotificationconfigv2"></a>
# **EditNotificationConfigV2**
> EditNotificationConfigV2200Response EditNotificationConfigV2 (EditNotificationConfigPayload editNotificationConfigPayload = null)

Edit an offset or system notification

Edit an existing offset notification, or enable/disable a system notification


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **editNotificationConfigPayload** | [**EditNotificationConfigPayload**](EditNotificationConfigPayload.md) | Offset or system notification updates | [optional]  |

### Return type

[**EditNotificationConfigV2200Response**](EditNotificationConfigV2200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getnotificationconfigv2"></a>
# **GetNotificationConfigV2**
> CreateNotificationConfigV2200Response GetNotificationConfigV2 (GetNotificationConfigPayload getNotificationConfigPayload = null)

Get an offset lifecycle event notification configuration

Retrieve a specific offset lifecycle event notification configuration by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **getNotificationConfigPayload** | [**GetNotificationConfigPayload**](GetNotificationConfigPayload.md) | Offset notification configuration ID | [optional]  |

### Return type

[**CreateNotificationConfigV2200Response**](CreateNotificationConfigV2200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Error |  -  |
| **404** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listoffsetnotificationconfigsv2"></a>
# **ListOffsetNotificationConfigsV2**
> ListOffsetNotificationConfigsV2200Response ListOffsetNotificationConfigsV2 (ListOffsetNotificationConfigsPayload listOffsetNotificationConfigsPayload = null)

List offset lifecycle event notification configurations

List offset lifecycle event notification configurations. These are user-created notifications that trigger at a specified time offset relative to lifecycle events. Returns a maximum of 400 results per request. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listOffsetNotificationConfigsPayload** | [**ListOffsetNotificationConfigsPayload**](ListOffsetNotificationConfigsPayload.md) | Optional pagination and filtering parameters | [optional]  |

### Return type

[**ListOffsetNotificationConfigsV2200Response**](ListOffsetNotificationConfigsV2200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listsystemnotificationconfigsv2"></a>
# **ListSystemNotificationConfigsV2**
> ListSystemNotificationConfigsV2200Response ListSystemNotificationConfigsV2 ()

List system notification types

List available system notification types. You can enable these notifications directly or use supported types to create offset notifications.


### Parameters
This endpoint does not need any parameter.
### Return type

[**ListSystemNotificationConfigsV2200Response**](ListSystemNotificationConfigsV2200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

