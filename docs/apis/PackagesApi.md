# Org.OpenAPITools.Api.PackagesApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchivePackageV1**](PackagesApi.md#archivepackagev1) | **POST** /v1/packages/archive | Archive a package |
| [**GetPackageV1**](PackagesApi.md#getpackagev1) | **POST** /v1/packages/get | Get a package |

<a id="archivepackagev1"></a>
# **ArchivePackageV1**
> ArchiveAlertV1200Response ArchivePackageV1 (ArchivePackageV1Request archivePackageV1Request = null)

Archive a package

Archive a package. Archived packages cannot be used to create new contracts. However, existing contracts associated with the package will continue to function as normal. Once you archive a package, you can still retrieve it in the UI and API, but you cannot unarchive it. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **archivePackageV1Request** | [**ArchivePackageV1Request**](ArchivePackageV1Request.md) |  | [optional]  |

### Return type

[**ArchiveAlertV1200Response**](ArchiveAlertV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Bad request |  -  |
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getpackagev1"></a>
# **GetPackageV1**
> GetPackageV1200Response GetPackageV1 (GetPackageV1Request getPackageV1Request = null)

Get a package

Gets the details for a specific package, including name, aliases, duration, and terms. Use this endpoint to understand a package’s alias schedule, or display a specific package’s details to end customers. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **getPackageV1Request** | [**GetPackageV1Request**](GetPackageV1Request.md) | Package ID | [optional]  |

### Return type

[**GetPackageV1200Response**](GetPackageV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

