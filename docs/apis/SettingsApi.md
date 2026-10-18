# Org.OpenAPITools.Api.SettingsApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveCreditTypeV1**](SettingsApi.md#archivecredittypev1) | **POST** /v1/credit-types/archive | Archive a pricing unit |
| [**CreateCreditTypeV1**](SettingsApi.md#createcredittypev1) | **POST** /v1/credit-types/create | Create a pricing unit |
| [**ListConfiguredBillingProvidersV1**](SettingsApi.md#listconfiguredbillingprovidersv1) | **POST** /v1/listConfiguredBillingProviders | List account-level billing providers |
| [**ListCreditTypesV1**](SettingsApi.md#listcredittypesv1) | **GET** /v1/credit-types/list | List pricing units |
| [**SetUpBillingProviderV1**](SettingsApi.md#setupbillingproviderv1) | **POST** /v1/setUpBillingProvider | Set up account-level billing provider |
| [**UpsertAnrokApiTokenV1**](SettingsApi.md#upsertanrokapitokenv1) | **POST** /v1/upsertAnrokApiToken | Upsert Anrok API token |
| [**UpsertAvalaraCredentialsV1**](SettingsApi.md#upsertavalaracredentialsv1) | **POST** /v1/upsertAvalaraCredentials | Upsert Avalara credentials |

<a id="archivecredittypev1"></a>
# **ArchiveCreditTypeV1**
> ArchiveAlertV1200Response ArchiveCreditTypeV1 (Id id = null)

Archive a pricing unit

Archive a custom pricing unit. Once archived, it will no longer appear in pricing unit selectors by default. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | [**Id**](Id.md) | The ID of the pricing unit to archive | [optional]  |

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
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createcredittypev1"></a>
# **CreateCreditTypeV1**
> ArchiveAlertV1200Response CreateCreditTypeV1 (CreateCreditTypeV1Request createCreditTypeV1Request = null)

Create a pricing unit

Create a custom pricing unit. Custom pricing units can be used to charge for usage in a non-fiat pricing unit, for example AI credits. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCreditTypeV1Request** | [**CreateCreditTypeV1Request**](CreateCreditTypeV1Request.md) |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listconfiguredbillingprovidersv1"></a>
# **ListConfiguredBillingProvidersV1**
> ListConfiguredBillingProvidersV1200Response ListConfiguredBillingProvidersV1 (ListConfiguredBillingProvidersV1Request listConfiguredBillingProvidersV1Request = null)

List account-level billing providers

Lists all configured billing providers and their delivery method configurations for your account. Returns provider details, delivery method IDs, and configuration settings needed for mapping individual customer contracts to billing integrations. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listConfiguredBillingProvidersV1Request** | [**ListConfiguredBillingProvidersV1Request**](ListConfiguredBillingProvidersV1Request.md) | Optional cursor to the next page of results | [optional]  |

### Return type

[**ListConfiguredBillingProvidersV1200Response**](ListConfiguredBillingProvidersV1200Response.md)

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listcredittypesv1"></a>
# **ListCreditTypesV1**
> ListCreditTypesV1200Response ListCreditTypesV1 (int limit = null, string nextPage = null)

List pricing units

List all pricing units. All fiat currency types (for example, USD or GBP) will be included, as well as any custom pricing units that were configured. Custom pricing units can be used to charge for usage in a non-fiat pricing unit, for example AI credits.  Note: The USD (cents) pricing unit is 2714e483-4ff1-48e4-9e25-ac732e8f24f2. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |

### Return type

[**ListCreditTypesV1200Response**](ListCreditTypesV1200Response.md)

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

<a id="setupbillingproviderv1"></a>
# **SetUpBillingProviderV1**
> SetUpBillingProviderV1200Response SetUpBillingProviderV1 (SetUpBillingProviderV1Request setUpBillingProviderV1Request = null)

Set up account-level billing provider

Set up account-level configuration for a billing provider. Once configured, individual contracts across customers can be mapped to this configuration using the returned delivery_method_id. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **setUpBillingProviderV1Request** | [**SetUpBillingProviderV1Request**](SetUpBillingProviderV1Request.md) | Billing provider, delivery method and configuration to insert | [optional]  |

### Return type

[**SetUpBillingProviderV1200Response**](SetUpBillingProviderV1200Response.md)

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
| **409** | Conflict error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="upsertanrokapitokenv1"></a>
# **UpsertAnrokApiTokenV1**
> UpsertAnrokApiTokenV1200Response UpsertAnrokApiTokenV1 (UpsertAnrokApiTokenV1Request upsertAnrokApiTokenV1Request = null)

Upsert Anrok API token

Set the Anrok API token for some specified delivery_method_ids, which can be found in the `/listConfiguredBillingProviders` response. This maps the Anrok key to the appropriate billing entity. These API tokens are only used for Threshold Billing workflows today. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **upsertAnrokApiTokenV1Request** | [**UpsertAnrokApiTokenV1Request**](UpsertAnrokApiTokenV1Request.md) | Set the Anrok API token for some specified delivery_method_ids | [optional]  |

### Return type

[**UpsertAnrokApiTokenV1200Response**](UpsertAnrokApiTokenV1200Response.md)

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

<a id="upsertavalaracredentialsv1"></a>
# **UpsertAvalaraCredentialsV1**
> Object UpsertAvalaraCredentialsV1 (UpsertAvalaraCredentialsV1Request upsertAvalaraCredentialsV1Request = null)

Upsert Avalara credentials

Set the Avalara credentials for some specified `delivery_method_ids`, which can be found in the `/listConfiguredBillingProviders` response. This maps the Avalara credentials to the appropriate billing entity. These credentials are only used for PLG Invoicing today. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **upsertAvalaraCredentialsV1Request** | [**UpsertAvalaraCredentialsV1Request**](UpsertAvalaraCredentialsV1Request.md) | Set the Avalara credentials for some specified &#x60;delivery_method_ids&#x60; | [optional]  |

### Return type

**Object**

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

