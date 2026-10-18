# Org.OpenAPITools.Api.DefaultApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListPackagesV1**](DefaultApi.md#listpackagesv1) | **POST** /v1/packages/list | List all packages |

<a id="listpackagesv1"></a>
# **ListPackagesV1**
> ListPackagesV1200Response ListPackagesV1 (int limit = null, string nextPage = null, ListPackagesV1Request listPackagesV1Request = null)

List all packages

Lists all packages with details including name, aliases, duration, and terms. To view contracts on a specific package, use the `listContractsOnPackage` endpoint. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **listPackagesV1Request** | [**ListPackagesV1Request**](ListPackagesV1Request.md) |  | [optional]  |

### Return type

[**ListPackagesV1200Response**](ListPackagesV1200Response.md)

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

